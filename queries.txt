Select *
Into Total_votes
From vine_table
Where total_votes >= 20;

Select *
Into helpful_votes_perc
From Total_Votes
Where Cast(helpful_votes AS FLOAT)/CAST(total_votes AS Float) >=0.5;

Select *
Into paid_vine
From helpful_votes_perc
Where vine = 'Y';

Select *
Into unpaid_vine
From helpful_votes_perc
Where vine = 'N';


Select Count (review_id)
From paid_vine;

Select Count (review_id)
From unpaid_vine;

Select COUNT (star_rating)
From paid_vine
Where star_rating = 5
limit 20

select *
from paid_vine
limit 50

with total as 
	(Select sum(total_votes) as totalvotes
	 From paid_vine), 
	 stars as 
	 (Select sum(total_votes) as totalvotes
	 From paid_vine
	 Where star_rating = 5)
Select total.totalvotes, stars.totalvotes as totalstars,
Round(Cast (stars.totalvotes as decimal)/Cast (total.totalvotes as decimal),2)
as paid_percentage
Into paid_perc
from total, stars


with total as 
	(Select sum(total_votes) as totalvotes
	 From unpaid_vine), 
	 stars as 
	 (Select sum(total_votes) as totalvotes
	 From unpaid_vine
	 Where star_rating = 5)
Select total.totalvotes, stars.totalvotes as totalstars,
Round(Cast (stars.totalvotes as decimal)/Cast (total.totalvotes as decimal),2)
as unpaid_percentage
Into unpaid_perc
from total, stars

select u.unpaid_percentage, p.paid_percentage
from unpaid_perc as u, paid_perc as p
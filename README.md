# Exploratory-data-anslysis
Exploratory data analysis using SQL and Excel data

Select count (*) 
from Superstore..[Orders$]

Select *
from Superstore..[Orders$]
order by 1

Select [Order ID], count(*)
from Superstore..[Orders$]
group by  [Order ID]
having count(*)>1

Select *
from Superstore..[Orders$]
where [Order ID] = 'MX-2012-155047'

Select *
from Superstore..[Orders$]
where [Ship Date]<[Order Date]

select distinct [Ship Mode] from Superstore..[Orders$]

Select min(a.Numofdays), max(a.Numofdays)
from(
Select DATEDIFF (day, [Order Date] , [Ship Date]) as Numofdays,*
from Superstore..[Orders$]
where [Ship Mode]= 'Second Class') a

Select min(a.Numofdays), max(a.Numofdays)
from(
Select DATEDIFF (day, [Order Date] , [Ship Date]) as Numofdays,*
from Superstore..[Orders$]
where [Ship Mode]= 'Same Day') a

Select [Customer ID], [Order ID], Count(*)
from Superstore..[Orders$]
group by [Customer ID], [Order ID]
order by [Order ID]

Select * 
from Superstore..[Orders$]
where [Order ID] ='AE-2011-9160'

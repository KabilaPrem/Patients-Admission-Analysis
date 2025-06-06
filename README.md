## 💼 Projects

### 🏥 Hospital Patient Analytics Dashboard
**Description:**  
Designed an interactive healthcare dashboard using Excel to visualize key metrics like patient satisfaction, readmission rates, and treatment patterns.

**Tools Used:**  
✔ Excel
✔ MySQL
✔ PowerPoint

**Used MYSQL for queries as well identifying KPIs**
## Total Patient:
```sql
select * from pt_rd
```
## Maximum Cost of each treatment:
```sql
select treatment,max(cost) from pt_rd group by treatment;
```
## Count of Age group based on health isse and gender:
```sql
select gender,health_issue,age,count(*) over (partition by gender order by age) as cnt from pt_rd group by gender,health_issue,age;
```
## percentage of readmission count:
```sql
select readmission,count(*)*100/(select count(*) from pt_rd) from pt_rd group by readmission;
```

**Highlights:**
- Cleaned and transformed raw data in Excel using PivotTables and slicers
- Queried structured patient data using MySQL joins and aggregations
- Created a dashboard to summarize key KPIs and trends
- Proposed actionable strategies to reduce readmission rates



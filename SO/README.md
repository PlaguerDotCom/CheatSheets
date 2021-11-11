# CheatSheet for the StackExchange Data Explorer


## User

```sql
select * from Users where DisplayName like '%pewdiepie%'
```

```sql
select * from Users where WebsiteUrl like '%plaguer%'
```

## Post

```sql
select top 50 * from Posts where AnswerCount > 50 order by AnswerCount desc
```

## More

```sql
select top 5 
u.Id as [User Link], p.Score as [Question Score], u.Reputation as [User Rep]
from Posts as p inner join Users as u on u.Id = p.OwnerUserId 
where p.PostTypeId = 1 
order by p.Score asc, u.Reputation desc
```
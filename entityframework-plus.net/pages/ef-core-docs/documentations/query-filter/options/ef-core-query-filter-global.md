---
Permalink: ef-core-query-filter-global
---

# Query Filter - Filter Global

Global filter can be used by any context.

Global filter is normally preferred in most scenarios over instance filter since the filter code is centralized in one method over being spread in multiple methods.

{% include template-example.html %} 
```csharp

// using Z.EntityFramework.Plus; // Don't forget to include this.
QueryFilterManager.Filter<Customer>(q => q.Where(x => x.IsActive));

var ctx = new EntitiesContext();
// TIP: You can also add this line in EntitiesContext constructor instead
QueryFilterManager.InitilizeGlobalFilter(ctx);

// SELECT * FROM Customer WHERE IsActive = true
var list = ctx.Customers.ToList();
```

[Try it](https://dotnetfiddle.net/IFndNf)

***Use entities context constructor to initialize global filter by default.***

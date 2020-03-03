# Interactive API


The Interactive API is an embedded GraphQL client that allows you to access all of your data with complete flexibility. Thanks to features like schema introspection and automatic authentication, the interactive API makes it simple to access Cloud. 

![](/cloud/ui/interactive-api.png)

You can also see the GraphQL API documentation directly inline.  Here you can find the queries and mutations you can run and see more information about what fields you can request (for queries) or change (for mutations).

![](/cloud/ui/interactive-api-inline-docs.png)

For example, to find out information about a specific flow, you could use a flow query.  The basics for that query would be:

```graphql
query {
    flow {
        name
        id
    }
}
```
You can also use the autocomplete to show what other fields you could query:

![](/cloud/ui/dropdown-on-interactive-api.png)

To get information about the tasks connected to your flow, you could use a nested query:

```graphql
query {
  flow {
    name 
    id
    tasks {
      name
    }
  }
}
```

Querrying for a all flows could return a lot of items!  To limit the number of items that are returned, you can use the 'Limit' selector at the top of the Interactive API page. The default limit is 10 and the maximum is 100. Inline limit arguments are overriden by the value set in the Limit selector. 

The 'Offset' selector lets you say where your queries should start. So for example, if my query returned 5 flows and I set the limit to 2 and the offset to 0, I would see the first 2 items returned from my query.  If I set the limit to 2 and the offset to 3, I would see the next 2 items.  

To search for a flow with a specific name, you can filter your search results, for example using the 'where' argument:

```graphql
query {
  flow (where: {name: {_eq: "My Flow Name"}}){
    name 
    id
    tasks {
      name
    }
  }
}
```

You can see more about query filters in the [Hasura Docs](https://hasura.io/docs/1.0/graphql/manual/queries/query-filters.html).





Docs for GQL mutations




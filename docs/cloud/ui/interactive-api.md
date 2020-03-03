# Interactive API


The Interactive API is an embedded GraphQL client that allows you to access all of your data with complete flexibility. Thanks to features like schema introspection and automatic authentication, the interactive API makes it simple to access Cloud. 

![](/cloud/ui/interactive-api.png)

You can also see the GraphQL API documentation directly inline.

For example, to find out information about a specific flow, you could use a flow query:

![](/cloud/ui/interactive-api-inline-docs.png)

```
query {
    flow {
        name
        id
    }
}
# Execute GraphQL Query with Hygraph

Executes a GraphQL query in Hygraph.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{endpoint}`
- **Official documentation:** [Execute GraphQL Query](https://hygraph.com/docs/api-reference/content-api/queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL query document to execute against the configured Hygraph Content API endpoint. |
| `variables` | body | `object` | no | Optional GraphQL variables object for the query. |

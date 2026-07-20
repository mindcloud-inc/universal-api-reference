# Execute GraphQL Mutation with Hygraph

Executes a GraphQL mutation in Hygraph.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{endpoint}`
- **Official documentation:** [Execute GraphQL Mutation](https://hygraph.com/docs/api-reference/content-api/mutations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL mutation document to execute against the configured Hygraph Content API endpoint. |
| `variables` | body | `object` | no | Optional GraphQL variables object for the mutation. |

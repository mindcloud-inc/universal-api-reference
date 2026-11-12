# Execute GraphQL with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [Execute GraphQL](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL query or mutation document to execute against Jobber. |
| `variables` | body | `string` | no | Optional GraphQL variables object encoded as JSON. |

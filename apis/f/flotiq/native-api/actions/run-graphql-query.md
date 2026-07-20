# Run GraphQL Query with Flotiq

Runs a GraphQL query against Flotiq.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.flotiq.com/api/v2/graphql`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Run GraphQL Query](https://flotiq.com/docs/API/graph-ql/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | The GraphQL query to execute. |
| `query` | body | `string` | yes | GraphQL query string to execute. |
| `variables` | body | `object` | no | Optional GraphQL variables object. |

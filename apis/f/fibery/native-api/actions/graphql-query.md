# GraphQL Query with Fibery

Retrieves query results from Fibery GraphQL.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql/space/:space`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [GraphQL Query](https://the.fibery.io/@public/User_Guide/Guide/GraphQL-queries-255)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `string` | yes | Fibery space name used in the GraphQL endpoint. |
| `query` | body | `string` | yes | GraphQL query text to execute. |

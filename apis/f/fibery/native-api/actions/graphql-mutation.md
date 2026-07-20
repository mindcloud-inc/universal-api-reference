# GraphQL Mutation with Fibery

Updates data in Fibery using GraphQL.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql/space/:space`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [GraphQL Mutation](https://the.fibery.io/@public/User_Guide/Guide/GraphQL-mutations-256)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `string` | yes | Fibery space name used in the GraphQL endpoint. |
| `query` | body | `string` | yes | GraphQL mutation text to execute. |

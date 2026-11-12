# List Clients with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `string` | no | Select the Jobber client fields to return. |
| `createdAfter` | body | `string` | no | Only return clients created after this timestamp (ISO 8601). Maps to filter.createdAt.after on the Jobber clients query. |
| `createdBefore` | body | `string` | no | Only return clients created before this timestamp (ISO 8601). Maps to filter.createdAt.before on the Jobber clients query. |
| `updatedAfter` | body | `string` | no | Only return clients updated after this timestamp (ISO 8601). Maps to filter.updatedAt.after on the Jobber clients query. |
| `updatedBefore` | body | `string` | no | Only return clients updated before this timestamp (ISO 8601). Maps to filter.updatedAt.before on the Jobber clients query. |
| `searchTerm` | body | `string` | no | Only return clients matching this Jobber search term. |

# Query Users with Sharetribe

Retrieves users from Sharetribe.

## Endpoint

- **Method:** `GET`
- **Path:** `users/query`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Query Users](https://www.sharetribe.com/api-reference/integration.html#query-users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdAtStart` | query | `date` | no | Filter users created on or after this ISO 8601 timestamp. |
| `createdAtEnd` | query | `date` | no | Filter users created before this ISO 8601 timestamp. |

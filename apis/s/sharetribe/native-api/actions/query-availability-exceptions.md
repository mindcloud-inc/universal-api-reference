# Query Availability Exceptions with Sharetribe

Retrieves availability exceptions from Sharetribe.

## Endpoint

- **Method:** `GET`
- **Path:** `availability_exceptions/query`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Query Availability Exceptions](https://www.sharetribe.com/api-reference/integration.html#query-availability-exceptions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listingId` | query | `string` | yes | The ID of the listing whose availability exceptions are queried. |
| `start` | query | `date` | yes | Query interval start time in ISO 8601 format. |
| `end` | query | `date` | yes | Query interval end time in ISO 8601 format. |

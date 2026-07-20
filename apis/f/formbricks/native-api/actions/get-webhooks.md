# Get Webhooks with Formbricks

Retrieves webhooks from Formbricks.

## Endpoint

- **Method:** `GET`
- **Path:** `/management/webhooks`
- **Base URL:** `https://app.formbricks.com/api/v2`
- **Official documentation:** [Get Webhooks](https://formbricks.com/docs/api-v2-reference/management-api--webhooks/get-webhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of webhooks to return. |
| `skip` | query | `number` | no | Number of webhooks to skip. |
| `sortBy` | query | `string` | no | Field to sort webhooks by. |
| `order` | query | `string` | no | Sort order. |
| `startDate` | query | `date` | no | Start date for filtering webhooks. |
| `endDate` | query | `date` | no | End date for filtering webhooks. |
| `filterDateField` | query | `string` | no | Date field to filter by. |
| `surveyIds` | query | `string` | no | Survey IDs to filter webhooks by. |

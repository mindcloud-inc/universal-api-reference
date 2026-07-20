# List Feedback with Retently

Retrieves a list of feedback responses from Retently.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/feedback`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [List Feedback](https://www.retently.com/api/#api-get-feedback-get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Search responses by a customer's email address; |
| `customerId` | query | `string` | no | Search responses by a customer's Retently ID; |
| `campaignId` | query | `string` | no | Filter responses by a specific campaign ID; |
| `page` | query | `string` | no | The current page number. Default 1; |
| `limit` | query | `string` | no | The items limit. Default 20. Maximum 1,000; |
| `sort` | query | `string` | no | The sort option. Use '-' for DESC. Default '-createdDate'; |
| `startDate` | query | `string` | no | ISO format or UNIX timestamp; |
| `endDate` | query | `string` | no | ISO format or UNIX timestamp; |
| `attributes[]` | query | `array<string>` | no | Filter by customer properties. See Attributes Filtering section below; |
| `match` | query | `string` | no | Logic for multiple attribute filters. Values: 'all' (AND, default), 'any' (OR); |
| `attributes[].name` | query | `string` | yes | Attribute field name |
| `attributes[].op` | query | `string` | yes | Filter operator |
| `attributes[].value` | query | `string` | yes | Attribute match value |

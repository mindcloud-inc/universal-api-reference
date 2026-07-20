# List Outbox with Retently

Retrieves a list of sent surveys from Retently.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/outbox`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [List Outbox](https://www.retently.com/api/#api-get-sent-surveys)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Find a customer's outbox records by email address; |
| `page` | query | `string` | no | The current page number. Default 1; |
| `limit` | query | `string` | no | The items limit. Default 20. Maximum 1,000; |
| `sort` | query | `string` | no | The sort option. Use '-surveyCreatedDate' for results in descending order; Default '-surveyCreatedDate'; |
| `campaignId` | query | `string` | no | Filter by campaign ID; |
| `startDate` | query | `string` | no | Filter surveys sent after this date. ISO format or UNIX timestamp; |
| `endDate` | query | `string` | no | Filter surveys sent before this date. ISO format or UNIX timestamp; |
| `channel` | query | `string` | no | Filter by survey channel. Values: email, link, inapp, intercom; |
| `sentBy` | query | `string` | no | Filter by how the survey was sent. Values: campaign, reminder, manual, test, imported; |
| `attributes[]` | query | `array<string>` | no | Filter by customer properties. See Attributes Filtering section below; |
| `match` | query | `string` | no | Logic for multiple attribute filters. Values: 'all' (AND, default), 'any' (OR); |
| `attributes[].name` | query | `string` | yes | Attribute field name |
| `attributes[].op` | query | `string` | yes | Filter operator |
| `attributes[].value` | query | `string` | yes | Attribute match value |

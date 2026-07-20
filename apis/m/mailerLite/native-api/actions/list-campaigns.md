# List Campaigns with MailerLite

Retrieves campaigns from MailerLite by status or type.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [List Campaigns](https://developers.mailerlite.com/docs/campaigns#campaign-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[status]` | query | `string` | no | Return campaigns by status: sent, draft, or ready. |
| `filter[type]` | query | `string` | no | Return campaigns by type: regular, ab, resend, or rss. |
| `limit` | query | `number` | no | Number of campaigns to return per page. |
| `page` | query | `number` | no | Page number to return. |

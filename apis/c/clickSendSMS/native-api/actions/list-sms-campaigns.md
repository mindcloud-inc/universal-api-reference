# List SMS Campaigns with ClickSend SMS

Retrieves SMS campaigns from ClickSend SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/sms-campaigns`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [List SMS Campaigns](https://developers.clicksend.com/docs/messaging/sms-campaigns/view-sms-campaigns/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `limit` | query | `number` | no |
| `q` | query | `string` | no |
| `order_by` | query | `string` | no |
| `date_from` | query | `number` | no |
| `date_to` | query | `number` | no |

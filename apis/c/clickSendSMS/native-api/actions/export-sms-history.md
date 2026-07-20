# Export SMS History with ClickSend SMS

Exports SMS history from ClickSend SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/sms/history/export`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Export SMS History](https://developers.clicksend.com/docs/messaging/sms/other/export-sms-history/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filename` | query | `string` | no |
| `page` | query | `number` | no |
| `limit` | query | `number` | no |
| `q` | query | `string` | no |
| `order_by` | query | `string` | no |
| `date_from` | query | `number` | no |
| `date_to` | query | `number` | no |

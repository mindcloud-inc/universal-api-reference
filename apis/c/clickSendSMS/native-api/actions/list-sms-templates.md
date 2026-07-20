# List SMS Templates with ClickSend SMS

Retrieves SMS templates from ClickSend SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/sms/templates`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [List SMS Templates](https://developers.clicksend.com/docs/messaging/sms/other/view-sms-templates/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `limit` | query | `number` | no |
| `q` | query | `string` | no |
| `order_by` | query | `string` | no |

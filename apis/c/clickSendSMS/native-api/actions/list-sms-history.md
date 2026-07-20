# List SMS History with ClickSend SMS

Retrieves SMS history from ClickSend SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/sms/history`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [List SMS History](https://developers.clicksend.com/docs/messaging/sms/other/view-sms-history)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search query for SMS history records. |
| `date_from` | query | `string` | no | Lower bound date filter for history. |
| `date_to` | query | `string` | no | Upper bound date filter for history. |
| `order_by` | query | `string` | no | Sort directive supported by ClickSend history endpoint. |

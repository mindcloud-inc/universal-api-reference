# List SMS Receipts with ClickSend SMS

Retrieves SMS receipts from ClickSend SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/sms/receipts`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [List SMS Receipts](https://developers.clicksend.com/docs/messaging/sms/other/view-sms-receipts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | query | `string` | no | Lower bound date filter for receipts. |
| `date_to` | query | `string` | no | Upper bound date filter for receipts. |

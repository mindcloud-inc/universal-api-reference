# List Numbers with ClickSend SMS

Retrieves dedicated numbers from ClickSend SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/numbers`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [List Numbers](https://developers.clicksend.com/docs/messaging/sender_ids/numbers/other/purchase-dedicated-number)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Items per page. |
| `q` | query | `string` | no | Search term for number records. |
| `exclude_10dlc_campaign` | query | `boolean` | no | Exclude 10DLC campaign details from response. |

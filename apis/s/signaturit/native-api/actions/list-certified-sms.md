# List Certified SMS with Signaturit

Retrieves certified SMS messages from Signaturit.

## Endpoint

- **Method:** `GET`
- **Path:** `/sms.json`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [List Certified SMS](https://docs.signaturit.com/api/latest#sms_get_sms)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Max number of SMS to retrieve. |
| `offset` | query | `number` | no | Results offset. |
| `status` | query | `string` | no | Filter SMS by status. |
| `since` | query | `string` | no | Return SMS sent on or after this date. |

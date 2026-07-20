# List SMS Replies with Notifyre SMS

Retrieves received SMS replies from Notifyre.

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/received`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [List SMS Replies](https://docs.notifyre.com/api/sms-received-list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromDate` | query | `string` | no | Inclusive start date filter for SMS replies. |
| `toDate` | query | `string` | no | Inclusive end date filter for SMS replies. |

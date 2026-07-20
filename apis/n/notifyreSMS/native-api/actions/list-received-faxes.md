# List Received Faxes with Notifyre SMS

Retrieves received fax messages from Notifyre.

## Endpoint

- **Method:** `GET`
- **Path:** `/fax/received`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [List Received Faxes](https://docs.notifyre.com/api/fax-received-list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromDate` | query | `string` | no | Inclusive start date filter for received faxes. |
| `toDate` | query | `string` | no | Inclusive end date filter for received faxes. |

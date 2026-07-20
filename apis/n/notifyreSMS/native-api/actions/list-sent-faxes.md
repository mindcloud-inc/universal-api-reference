# List Sent Faxes with Notifyre SMS

Retrieves sent fax messages from Notifyre.

## Endpoint

- **Method:** `GET`
- **Path:** `/fax/send`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [List Sent Faxes](https://docs.notifyre.com/api/fax-sent-list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromDate` | query | `string` | no | Inclusive start date filter for sent faxes. |
| `statusType` | query | `string` | no | Status filter for sent faxes. |
| `toDate` | query | `string` | no | Inclusive end date filter for sent faxes. |

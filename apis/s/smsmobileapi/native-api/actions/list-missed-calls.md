# List Missed Calls with Smsmobileapi

Retrieves missed calls from Smsmobileapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/call/missed/list/`
- **Base URL:** `https://api.smsmobileapi.com`
- **Official documentation:** [List Missed Calls](https://smsmobileapi.com/doc-call/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offset` | query | `number` | no | Pagination offset. The provider defaults this to 0. |
| `limit` | query | `number` | no | Maximum number of rows to return. The provider defaults to 100 and caps at 500. |
| `search` | query | `string` | no | Search by caller number or cached contact name. |
| `date_start` | query | `date` | no | Only include calls from this day onward. |
| `date_end` | query | `date` | no | Only include calls up to this day. |

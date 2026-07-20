# List Leads with Callingly

Retrieves leads from Callingly.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/leads`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [List Leads](https://help.callingly.com/article/38-callingly-api-documentation#List-Leads-_hyZk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | Filter leads created on or before this date in YYYY-MM-DD format. |
| `phone_number` | query | `string` | no | Filter leads by phone number. |
| `start` | query | `string` | no | Filter leads created on or after this date in YYYY-MM-DD format. |

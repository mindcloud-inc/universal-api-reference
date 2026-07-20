# List Event Hooks with Signaturit

Retrieves event hooks from Signaturit.

## Endpoint

- **Method:** `GET`
- **Path:** `/event-hooks`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [List Event Hooks](https://docs.signaturit.com/api/latest#eventhooks_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to fetch. Defaults to 1. |
| `date` | query | `string` | no | Stringified JSON date range like {"from":"2023-03-01","to":"2023-03-28"}. |
| `status` | query | `list<number>` | no | One or more event-hook HTTP status codes to match. Send multiple values as a array. |
| `method` | query | `list<string>` | no | One or more HTTP methods to match, for example POST or GET. Send multiple values as a array. |
| `search` | query | `string` | no | Search string to match event-hook records. |

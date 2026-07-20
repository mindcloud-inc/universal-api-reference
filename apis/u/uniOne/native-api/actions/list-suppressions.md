# List Suppressions with UniOne

Retrieves suppressions from UniOne with optional filters.

## Endpoint

- **Method:** `POST`
- **Path:** `suppression/list.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [List Suppressions](https://docs.unione.io/en/web-api-ref#suppression-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cause` | body | `string` | no | Optional suppression cause filter. |
| `source` | body | `string` | no | Optional suppression source filter. |
| `start_time` | body | `string` | no | Optional UTC start time in YYYY-MM-DD hh:mm:ss format. |
| `cursor` | body | `string` | no | Continuation cursor from the previous suppression list response. |

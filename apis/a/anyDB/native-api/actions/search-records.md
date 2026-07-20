# Search Records with AnyDB

Finds records in AnyDB by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integrations/ext/search`
- **Base URL:** `https://app.anydb.com`
- **Official documentation:** [Search Records](https://www.anydb.com/openapi/spec.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adbid` | query | `string` | yes | The AnyDB database ID. |
| `teamid` | query | `string` | yes | The AnyDB team ID. |
| `search` | query | `string` | yes | The text to search for. |
| `parentid` | query | `string` | no | Optional parent record ID to scope the search. |
| `start` | query | `number` | no | Optional starting offset for the search. |
| `limit` | query | `number` | no | Optional maximum number of search results. |

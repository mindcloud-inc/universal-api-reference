# List Tags with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/get`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [List Tags](https://help.ortto.com/a-263-retrieve-a-list-of-tags-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | body | `string` | no | Search tag names. Ortto splits the value into tokens and matches all tokens. |

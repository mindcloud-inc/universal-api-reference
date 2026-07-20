# List Audiences with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/audiences/get`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [List Audiences](https://help.ortto.com/a-268-retrieve-a-list-of-audiences-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_term` | body | `string` | no | Audience search term. |
| `with_filter` | body | `boolean` | no | Only return audiences with a filter configured. |
| `archived` | body | `boolean` | no | Include archived audiences. |
| `retention` | body | `string` | no | Audience retention type. |
| `limit` | body | `number` | no | Maximum number of audiences to return. |
| `offset` | body | `number` | no | Number of audiences to skip. |

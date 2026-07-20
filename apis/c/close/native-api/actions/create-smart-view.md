# Create Smart View with Close

Creates a new smart view in Close.

## Endpoint

- **Method:** `POST`
- **Path:** `/saved_search/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Create Smart View](https://developer.close.com/resources/smart-views/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Smart view name. |
| `query` | body | `string` | no | Smart view query payload. |
| `type` | body | `string` | yes | Smart view type. |

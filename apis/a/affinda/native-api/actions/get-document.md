# Get specific document with Affinda

Retrieves a specific document from Affinda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/documents/:identifier`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Get specific document](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `compact` | query | `string` | no | If "true", the response is compacted to annotations' parsed data. Annotations' meta data are excluded. Default is "false". |
| `format` | query | `string` | no | Specify which format you want the response to be. Default is "json" |
| `identifier` | path | `string` | yes | Document's identifier |
| `snake_case` | query | `string` | no | Whether to return the response in snake_case instead of camelCase. Default is false. |

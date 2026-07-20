# List Analyses with DocuPanda - Document Understanding

Retrieves analyses from DocuPanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/analyses`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [List Analyses](https://docs.docupipe.ai/reference/list_analyses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The maximum number of analyses to return. maximum is 20 |
| `offset` | query | `number` | no | The number of analyses to skip (to paginate through the data) |

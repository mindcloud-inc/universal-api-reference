# List Flow Results with Base64.ai

Retrieves results from a specific Base64.ai flow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/result`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [List Flow Results](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowID` | query | `string` | yes | Flow identifier whose results should be listed. |
| `limit` | query | `number` | no | Maximum number of results to return. |

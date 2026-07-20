# Extract Data with Kadoa

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/adhoc/:schemaId`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Extract Data](https://docs.kadoa.com/api-reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `link` | body | `string` | yes | URL to extract from |
| `schemaId` | path | `string` | yes | Schema ID or: html, body, markdown |

# Poll Extract with DocumentPro

Retrieves an extract job result from DocumentPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/files`
- **Base URL:** `https://api.documentpro.ai`
- **Official documentation:** [Poll Extract](https://docs.documentpro.ai/docs/using-api/extract/get-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | query | `string` | yes | The request_id returned from Run Extract. |

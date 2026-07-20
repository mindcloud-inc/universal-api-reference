# Download Resource with Freepik

Retrieves a Freepik resource download URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/resources/{{resource-id}}/download`
- **Base URL:** `https://api.freepik.com`
- **Official documentation:** [Download Resource](https://docs.freepik.com/api-reference/resources/download-a-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource-id` | path | `number` | yes | Freepik resource identifier to download. |

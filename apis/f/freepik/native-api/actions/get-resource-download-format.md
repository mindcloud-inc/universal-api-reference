# Get Resource Download Format with Freepik

Retrieves a Freepik resource download in a specified format.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/resources/{{resource-id}}/download/{{resource-format}}`
- **Base URL:** `https://api.freepik.com`
- **Official documentation:** [Get Resource Download Format](https://docs.freepik.com/api-reference/resources/images-and-templates-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource-id` | path | `number` | yes | Freepik resource identifier. |
| `resource-format` | path | `string` | yes | Download format to request for the resource, such as eps when available. |

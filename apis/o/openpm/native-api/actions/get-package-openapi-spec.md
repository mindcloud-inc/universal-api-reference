# Get Package OpenAPI Spec with openpm

## Endpoint

- **Method:** `GET`
- **Path:** `/packages/:packageId/openapi`
- **Base URL:** `https://openpm.ai/api`
- **Official documentation:** [Get Package OpenAPI Spec](https://openpm.ai/apis/openpm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `string` | yes | Package ID. |
| `format` | query | `list` | no | OpenAPI spec format. Supported values are json and yaml. Accepted values: `0`, `1`. |

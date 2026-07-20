# List Traces with Langbase

## Endpoint

- **Method:** `GET`
- **Path:** `v1/traces`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [List Traces](https://langbase.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `primitiveId` | query | `string` | yes | Primitive ID to filter traces by. |
| `primitiveName` | query | `string` | yes | Primitive name to filter traces by. |
| `limit` | query | `number` | no | Maximum number of traces to return. |
| `offset` | query | `number` | no | Number of traces to skip. |
| `order` | query | `list` | no | Sort order for traces. Accepted values: `0`, `1`. |

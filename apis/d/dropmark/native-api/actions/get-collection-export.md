# Get Collection Export with Dropmark

## Endpoint

- **Method:** `GET`
- **Path:** `/{{args.collectionId}}.{{args.format}}`
- **Base URL:** `https://{subdomain}`
- **Official documentation:** [Get Collection Export](https://support.dropmark.com/article/96-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `number` | yes | Numeric Dropmark collection identifier. |
| `format` | path | `string` | yes | Raw collection export representation. Accepted values: `0`, `1`, `2`, `3`. |
| `key` | query | `string` | yes | Collection-specific read-only key from Collection Settings > Advanced > JSON. Required for private collections unless you use basic auth outside this app contract. |

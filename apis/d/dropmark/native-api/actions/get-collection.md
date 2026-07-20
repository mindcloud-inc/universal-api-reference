# Get Collection with Dropmark

## Endpoint

- **Method:** `GET`
- **Path:** `/{{args.collectionId}}.json`
- **Base URL:** `https://{subdomain}`
- **Official documentation:** [Get Collection](https://support.dropmark.com/article/96-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `number` | yes | Numeric Dropmark collection identifier. |
| `key` | query | `string` | yes | Collection-specific read-only key from Collection Settings > Advanced > JSON. Required for private collections unless you use basic auth outside this app contract. |
| `callback` | query | `string` | no | Optional JSONP callback name supported by Dropmark collection JSON feeds. |

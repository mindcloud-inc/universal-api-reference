# Get Collection RSS with Dropmark

## Endpoint

- **Method:** `GET`
- **Path:** `/{{args.collectionId}}.rss`
- **Base URL:** `https://{subdomain}`
- **Official documentation:** [Get Collection RSS](https://support.dropmark.com/article/96-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `number` | yes | Numeric Dropmark collection identifier. |
| `key` | query | `string` | yes | Collection-specific read-only key from Collection Settings > Advanced > JSON. |

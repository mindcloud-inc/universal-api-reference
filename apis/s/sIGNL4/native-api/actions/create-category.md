# Create Category with SIGNL4

Creates a category in SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/categories/{teamId}`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Create Category](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | ID of the team the category belongs to |
| `id` | body | `string` | no | — |
| `teamId` | body | `string` | no | — |
| `isDefault` | body | `boolean` | no | — |
| `options` | body | `number` | no | <p/><ul><li>0 = None</li><li>1 = Hidden</li><li>2 = DenyDelete</li><li>4 = HideOptOut</li><li>8 = HideKeywords</li></ul> |
| `name` | body | `string` | yes | — |
| `color` | body | `string` | yes | — |
| `imageName` | body | `string` | yes | — |
| `keywords[]` | body | `array<string>` | yes | — |
| `keywordsExcluded[]` | body | `array<string>` | no | — |
| `keywordMatching` | body | `number` | yes | <p/><ul><li>0 = Any</li><li>1 = All</li></ul> |
| `augmentations[]` | body | `array<object>` | no | — |
| `enrichments[]` | body | `array<object>` | no | — |
| `order` | body | `number` | no | — |

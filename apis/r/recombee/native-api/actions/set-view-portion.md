# Set View Portion with Recombee

Creates a view portion event in Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/viewportions/`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Set View Portion](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `itemId` | body | `string` | yes |
| `portion` | body | `string` | no |
| `userId` | body | `string` | yes |

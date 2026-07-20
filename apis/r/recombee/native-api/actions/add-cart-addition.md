# Add Cart Addition with Recombee

Creates a cart addition event in Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/cartadditions/`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Add Cart Addition](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `itemId` | body | `string` | yes |
| `userId` | body | `string` | yes |

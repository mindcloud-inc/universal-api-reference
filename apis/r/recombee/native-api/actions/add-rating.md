# Add Rating with Recombee

Creates a rating event in Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/ratings/`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Add Rating](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `itemId` | body | `string` | yes |
| `rating` | body | `string` | no |
| `userId` | body | `string` | yes |

# Add Purchase with Recombee

Creates a purchase event in Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/purchases/`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Add Purchase](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `itemId` | body | `string` | yes |
| `userId` | body | `string` | yes |

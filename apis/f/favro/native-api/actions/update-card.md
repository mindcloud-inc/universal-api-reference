# Update Card with Favro

Updates an existing card in Favro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/cards/:cardId`
- **Base URL:** `https://favro.com/api/v1`
- **Official documentation:** [Update Card](https://favro.com/developer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | The card ID to update. |
| `name` | body | `string` | no | The new card name. |

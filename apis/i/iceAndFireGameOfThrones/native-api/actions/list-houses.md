# List Houses with Ice and Fire (Game of Thrones)

## Endpoint

- **Method:** `GET`
- **Path:** `/houses`
- **Base URL:** `https://anapioficeandfire.com/api`
- **Official documentation:** [List Houses](https://github.com/joakimskoog/AnApiOfIceAndFire/wiki/Houses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Return only houses with this exact name. |
| `region` | query | `string` | no | Return only houses from this region. |
| `words` | query | `string` | no | Return only houses with these words. |
| `hasWords` | query | `boolean` | no | Return only houses that do or do not have words. |
| `hasTitles` | query | `boolean` | no | Return only houses that do or do not have titles. |
| `hasSeats` | query | `boolean` | no | Return only houses that do or do not have seats. |
| `hasDiedOut` | query | `boolean` | no | Return only houses that have or have not died out. |
| `hasAncestralWeapons` | query | `boolean` | no | Return only houses that do or do not have ancestral weapons. |

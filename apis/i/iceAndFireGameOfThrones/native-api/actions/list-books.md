# List Books with Ice and Fire (Game of Thrones)

## Endpoint

- **Method:** `GET`
- **Path:** `/books`
- **Base URL:** `https://anapioficeandfire.com/api`
- **Official documentation:** [List Books](https://github.com/joakimskoog/AnApiOfIceAndFire/wiki/Books)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Return books with this exact name. |
| `fromReleaseDate` | query | `date` | no | Return books released on or after this date. |
| `toReleaseDate` | query | `date` | no | Return books released on or before this date. |

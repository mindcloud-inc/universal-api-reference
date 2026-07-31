# List Characters with Ice and Fire (Game of Thrones)

## Endpoint

- **Method:** `GET`
- **Path:** `/characters`
- **Base URL:** `https://anapioficeandfire.com/api`
- **Official documentation:** [List Characters](https://github.com/joakimskoog/AnApiOfIceAndFire/wiki/Characters)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Return only characters with this exact name. |
| `gender` | query | `string` | no | Return only characters with this gender. |
| `culture` | query | `string` | no | Return only characters from this culture. |
| `born` | query | `string` | no | Return only characters born in this year string. |
| `died` | query | `string` | no | Return only characters who died in this year string. |
| `isAlive` | query | `boolean` | no | Return only characters who are alive or dead. |

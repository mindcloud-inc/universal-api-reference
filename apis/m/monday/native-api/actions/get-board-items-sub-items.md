# Get Board Items with Sub Items with Monday

Retrieves board items and subitems from a Monday board.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.monday.com/v2/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `boardId` | body | `number` | no |
| `columnId` | body | `string` | no |
| `compareValue[]` | body | `array<string>` | no |

# Get All SubItems Of Of an Item by Item's Column Value with Monday

Retrieves items and their subitems from a Monday board by column value.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.monday.com/v2/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `columnId` | body | `string` | no |
| `compareValue[]` | body | `array<string>` | no |
| `boardId` | body | `number` | no |

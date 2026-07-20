# Get Board Items by Column Value with Monday

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.monday.com/v2/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `boardId` | body | `number` | no |
| `boardFields` | body | `string` | no |
| `columnId` | body | `string` | no |
| `compareValue[]` | body | `array<string>` | no |
| `itemFields` | body | `string` | no |

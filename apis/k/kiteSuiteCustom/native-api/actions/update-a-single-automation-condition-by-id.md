# Update a single automation condition by ID with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/automation/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update a single automation condition by ID](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The automation condition ID |
| `workspace` | body | `string` | no | — |
| `createdBy` | body | `string` | no | — |
| `eventType` | body | `string` | no | — |
| `trigger` | body | `object` | no | — |
| `events[]` | body | `array` | no | — |
| `actions[]` | body | `array` | no | — |
| `description` | body | `string` | no | — |
| `isActive` | body | `boolean` | no | — |
| `isTrashed` | body | `boolean` | no | — |

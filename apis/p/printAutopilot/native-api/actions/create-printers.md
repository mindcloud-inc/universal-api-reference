# Create Printers with Print Autopilot

Creates printers in Print Autopilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/printers`
- **Base URL:** `https://printautopilot.com/api`
- **Official documentation:** [Create Printers](https://documenter.getpostman.com/view/1334461/TW6wJonb#f3ab1c25-42d7-4be5-8be5-4027b78feffb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | no | Printer objects to create. |
| `items[].name` | body | `string` | no | — |
| `items[].paperSizes[]` | body | `array<object>` | no | — |
| `items[].paperSizes[].name` | body | `string` | no | — |
| `items[].paperSizes[].height` | body | `number` | no | — |
| `items[].paperSizes[].width` | body | `number` | no | — |
| `items[].paperSizes[].rawKind` | body | `string` | no | — |

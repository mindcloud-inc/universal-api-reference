# List Estimates with Harpoon

Retrieves estimates from Harpoon.

## Endpoint

- **Method:** `GET`
- **Path:** `/estimates`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [List Estimates](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `year` | query | `number` | no |
| `clients[]` | query | `array<number>` | no |
| `projects[]` | query | `array<number>` | no |
| `status` | query | `string` | no |
| `search` | query | `string` | no |

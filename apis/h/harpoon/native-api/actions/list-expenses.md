# List Expenses with Harpoon

Retrieves expenses from Harpoon.

## Endpoint

- **Method:** `GET`
- **Path:** `/expenses`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [List Expenses](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_date` | query | `date` | no |
| `end_date` | query | `date` | no |
| `clients[]` | query | `array<number>` | no |
| `projects[]` | query | `array<number>` | no |
| `categories[]` | query | `array<number>` | no |
| `status` | query | `string` | no |
| `search` | query | `string` | no |

# List Time Entries with Harpoon

Retrieves time entries from Harpoon.

## Endpoint

- **Method:** `GET`
- **Path:** `/time_entries`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [List Time Entries](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status` | query | `string` | no |
| `start` | query | `date` | no |
| `end` | query | `date` | no |
| `clients[]` | query | `array<number>` | no |
| `projects[]` | query | `array<number>` | no |
| `tasks[]` | query | `array<number>` | no |
| `profiles[]` | query | `array<number>` | no |
| `statuses[]` | query | `array<string>` | no |

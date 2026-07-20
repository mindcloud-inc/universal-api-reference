# Create Person with Follow Up Boss

Creates a new person in Follow Up Boss.

## Endpoint

- **Method:** `POST`
- **Path:** `people`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [Create Person](https://docs.followupboss.com/reference/people-post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `source` | body | `string` | no |
| `sourceUrl` | body | `string` | no |
| `stage` | body | `string` | no |
| `assignedTo` | body | `string` | no |
| `contacted` | body | `boolean` | no |
| `createdAt` | body | `date` | no |
| `emails[].value` | body | `string` | no |
| `emails[].type` | body | `string` | no |
| `emails[].isPrimary` | body | `boolean` | no |
| `phones[].value` | body | `string` | no |
| `phones[].type` | body | `string` | no |
| `phones[].isPrimary` | body | `boolean` | no |
| `addresses[].type` | body | `string` | no |
| `addresses[].street` | body | `string` | no |
| `addresses[].city` | body | `string` | no |
| `addresses[].state` | body | `string` | no |
| `addresses[].code` | body | `string` | no |
| `addresses[].country` | body | `string` | no |
| `tags[]` | body | `array<string>` | no |

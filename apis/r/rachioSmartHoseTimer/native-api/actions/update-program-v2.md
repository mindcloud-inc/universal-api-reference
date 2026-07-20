# Update Program V2 with Rachio Smart Hose Timer

Updates an existing program in Rachio.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://cloud-rest.rach.io/program/updateProgramV2`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Update Program V2](https://rachio.readme.io/reference/programservice_updateprogramv2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | no |
| `name` | body | `string` | no |
| `color` | body | `string` | no |
| `enabled` | body | `boolean` | no |
| `dailyInterval` | body | `object` | no |
| `daysOfWeek` | body | `object` | no |
| `oddDays` | body | `string` | no |
| `evenDays` | body | `string` | no |
| `plannedRuns[]` | body | `array<object>` | no |
| `rainSkipEnabled` | body | `boolean` | no |
| `settings` | body | `object` | no |

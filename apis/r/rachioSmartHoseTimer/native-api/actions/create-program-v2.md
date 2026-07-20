# Create Program V2 with Rachio Smart Hose Timer

Creates a new program in Rachio.

## Endpoint

- **Method:** `POST`
- **Path:** `https://cloud-rest.rach.io/program/createProgramV2`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Create Program V2](https://rachio.readme.io/reference/programservice_createprogramv2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `color` | body | `string` | no |
| `dailyInterval` | body | `object` | no |
| `daysOfWeek` | body | `object` | no |
| `oddDays` | body | `string` | no |
| `evenDays` | body | `string` | no |
| `plannedRuns[]` | body | `array<object>` | no |
| `rainSkipEnabled` | body | `boolean` | no |
| `settings` | body | `object` | no |

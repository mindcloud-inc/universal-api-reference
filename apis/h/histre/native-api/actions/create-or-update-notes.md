# Create Or Update Notes with Histre

Creates or updates notes in Histre.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/note/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Create Or Update Notes](https://histre.com/features/api/notes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `append` | query | `string` | no | Optional append mode. Use always, dedupe, or true. |
| `attrpriority` | query | `string` | no | Optional attribute priority strategy. Use old or new. |
| `notify` | query | `boolean` | no | Set false to suppress notifications to users with access to affected collections. |
| `notes[]` | body | `array<object>` | yes | Array of one or more Histre note objects to create or update. |

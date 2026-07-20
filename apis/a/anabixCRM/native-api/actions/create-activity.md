# Create Activity with Anabix CRM

Creates a new activity in Anabix CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.anabix.cz`
- **Official documentation:** [Create Activity](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Activity body. Anabix requires body when creating an activity. |
| `idContact` | body | `number` | yes | — |
| `title` | body | `string` | no | Optional activity title. If omitted, Anabix creates a title from the activity body. |
| `type` | body | `string` | no | Activity type, such as note, call, meeting, email, or SMS. |

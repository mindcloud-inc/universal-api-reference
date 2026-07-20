# Create Person Timeline Note with Lunatask

## Endpoint

- **Method:** `POST`
- **Path:** `/person_timeline_notes`
- **Base URL:** `https://api.lunatask.app/v1`
- **Official documentation:** [Create Person Timeline Note](https://lunatask.app/api/person-timeline-notes-api/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person_id` | body | `string` | yes | The Person ID of the person for the timeline note |
| `date_on` | body | `date` | no | ISO-8601 formatted date for the timeline note |
| `content` | body | `string` | no | The content of the timeline note in Markdown |

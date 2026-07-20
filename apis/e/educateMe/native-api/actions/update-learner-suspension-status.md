# Update Learner Suspension Status with EducateMe

Updates a learner's suspension status in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/students/:email`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Update Learner Suspension Status](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#7f8ba3abfef0443fb86e07842361b6d8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Learner email. |
| `isSuspended` | body | `boolean` | yes | Whether the learner is suspended. |

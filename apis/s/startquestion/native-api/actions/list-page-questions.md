# List Page Questions with Startquestion

Retrieves questions for a Startquestion survey page.

## Endpoint

- **Method:** `GET`
- **Path:** `/questions/:id_survey/:id_page`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [List Page Questions](https://help.startquestion.com/en/articles/5809873-questions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Probe arg. |
| `id_survey` | path | `number` | yes | Survey ID. |
| `id_page` | path | `number` | yes | Page ID. |

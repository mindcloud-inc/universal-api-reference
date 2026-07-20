# Update Roadmap Card with LoopedIn

Updates an existing roadmap card in LoopedIn.

## Endpoint

- **Method:** `PUT`
- **Path:** `/roadmap-cards/:id`
- **Base URL:** `https://api.loopedin.io/v1`
- **Official documentation:** [Update Roadmap Card](https://docs.loopedin.io/#update-roadmap-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LoopedIn roadmap card ID. |
| `title` | body | `string` | no | The updated roadmap card title. |

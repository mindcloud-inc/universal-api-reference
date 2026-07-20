# Create Roadmap Card with LoopedIn

Creates a new roadmap card in LoopedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/roadmap-cards`
- **Base URL:** `https://api.loopedin.io/v1`
- **Official documentation:** [Create Roadmap Card](https://docs.loopedin.io/#create-roadmap-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `column` | body | `string` | yes | The LoopedIn roadmap column ID. |
| `objective` | body | `string` | yes | The LoopedIn roadmap objective ID. |
| `title` | body | `string` | yes | The roadmap card title. |
| `workspace_id` | body | `string` | yes | The LoopedIn workspace ID. |

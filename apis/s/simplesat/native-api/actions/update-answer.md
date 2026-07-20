# Update Answer with Simplesat

Updates an existing answer in Simplesat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/answers/:answer_id`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [Update Answer](https://developer.simplesat.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `answer_id` | path | `string` | yes | The ID of the answer to update |
| `choice` | body | `string` | no | — |
| `choices[]` | body | `array<string>` | no | — |
| `comment` | body | `string` | no | — |
| `follow_up_answer` | body | `string` | no | — |
| `follow_up_answer_choice` | body | `string` | no | — |
| `follow_up_answer_choices[]` | body | `array<string>` | no | — |

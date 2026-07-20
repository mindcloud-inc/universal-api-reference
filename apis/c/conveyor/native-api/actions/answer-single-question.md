# Answer Single Question with Conveyor

Answers a one-off question in Conveyor.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/single_question`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [Answer Single Question](https://docs.conveyor.com/reference/post-single-question)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `question` | body | `string` | yes | Question to answer. |
| `product_line_ids` | body | `string<string>` | no | Product line identifiers to use as answer context. |
| `question_type` | body | `string` | no | Question type. |
| `multiple_choice_options[]` | body | `array<string>` | no | Multiple choice answer options. |
| `confidence_threshold` | body | `string` | no | Minimum confidence threshold. |
| `email` | body | `string` | no | Requester email address. |

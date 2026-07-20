# Create Question with ClassMarker

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/questions.json`
- **Base URL:** `https://api.classmarker.com`
- **Official documentation:** [Create Question](https://www.classmarker.com/online-testing/docs/api/#post-question)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `question` | body | `string` | yes | Question text shown to exam takers. |
| `question_type` | body | `string` | yes | Writable ClassMarker question type: multiplechoice, multipleresponse, truefalse, or essay. |
| `category_id` | body | `number` | yes | Numeric ClassMarker category ID that owns the question. |
| `points` | body | `number` | yes | Points awarded for a correct answer. |
| `random_answers` | body | `boolean` | no | Whether ClassMarker should randomize answer order for supported question types. |
| `options` | body | `object` | no | Options object keyed by letter (for example A, B, C) for supported question types. |
| `correct_options[]` | body | `array<string>` | no | Option letters that are correct for the question type. |
| `grade_style` | body | `string` | no | Multiple response grading style: partial_with_deduction, partial_without_deduction, or off. |
| `correct_feedback` | body | `string` | no | Feedback shown for a correct answer. |
| `incorrect_feedback` | body | `string` | no | Feedback shown for an incorrect answer. |
| `verify_only` | query | `boolean` | no | Validate the request without creating the question. |

# Update Starter Question with Botsonic

Updates an existing starter question in Botsonic.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/business/bot-starter-questions/:starterQuestionId`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Update Starter Question](https://docs.botsonic.com/reference/update_starter_question_v1_business_bot_starter_questions__starter_question_id__patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `starter_question_id` | path | `string` | yes | starter_question_id of the starter question. |
| `question` | body | `string` | no | Updated starter question text. |
| `answer` | body | `string` | no | Updated answer for the starter question. |
| `order` | body | `number` | no | Updated display order. |

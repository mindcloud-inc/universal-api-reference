# Create Starter Question with Botsonic

Creates a new starter question in Botsonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/business/bot-starter-questions`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Create Starter Question](https://docs.botsonic.com/reference/create_starter_question_v1_business_bot_starter_questions_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `question` | body | `string` | yes | Starter question text. |
| `answer` | body | `string` | yes | Answer shown for the starter question. |
| `order` | body | `number` | no | Display order. |

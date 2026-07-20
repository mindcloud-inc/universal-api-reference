# Create FAQ with Botsonic

Creates a new FAQ in Botsonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/business/bot-faq`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Create FAQ](https://docs.botsonic.com/reference/create_single_faq_v1_business_bot_faq_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `question` | body | `string` | yes | FAQ question. |
| `answer` | body | `string` | yes | FAQ answer. |

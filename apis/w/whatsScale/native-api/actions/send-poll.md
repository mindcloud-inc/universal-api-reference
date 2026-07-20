# Send Poll with WhatsScale

Sends a poll message through WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sendPoll`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Send Poll](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | body | `string` | yes | Recipient chat ID. |
| `multipleAnswers` | body | `boolean` | no | Allow respondents to select multiple poll options. |
| `options[]` | body | `array<string>` | yes | Array of 2-12 unique poll options. Send multiple values as a array. |
| `question` | body | `string` | yes | Poll question. |
| `session` | body | `string` | yes | Session name from /api/sessions. |

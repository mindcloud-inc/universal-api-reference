# Submit User Feedback with Vistaly

Creates user feedback in Vistaly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/feedback`
- **Base URL:** `https://api.vistaly.com`
- **Official documentation:** [Submit User Feedback](https://docs.vistaly.com/api-reference/feedback/submit-user-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | The content of the feedback. |
| `cardIds[]` | body | `array<string>` | no | Optional card IDs to associate with this feedback. |
| `feedbackProviders[]` | body | `array<object>` | no | People who provided the feedback. |
| `feedbackReceivers[]` | body | `array<object>` | no | People who received the feedback. |
| `parseMarkdown` | body | `boolean` | no | Whether to parse the body as markdown. |
| `timestamp` | body | `date` | no | When the feedback was captured. |
| `url` | body | `string` | no | The URL where the feedback came from. |

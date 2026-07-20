# Submit Interview Data with Vistaly

Creates interview data in Vistaly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/interviews`
- **Base URL:** `https://api.vistaly.com`
- **Official documentation:** [Submit Interview Data](https://docs.vistaly.com/api-reference/interviews/submit-interview-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | The interview notepad content. |
| `cardIds[]` | body | `array<string>` | no | Optional card IDs to associate with this interview. |
| `feedbackProviders[]` | body | `array<object>` | no | People who provided the interview. |
| `feedbackReceivers[]` | body | `array<object>` | no | People who conducted the interview. |
| `parseMarkdown` | body | `boolean` | no | Whether to parse the body as markdown. |
| `timestamp` | body | `date` | no | When the interview was captured. |
| `url` | body | `string` | no | The URL where the interview came from. |

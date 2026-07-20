# Submit AI Invocation Feedback with Port API AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/ai/invoke/:invocation_identifier/feedback`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Submit AI Invocation Feedback](https://docs.port.io/api-reference/submit-ai-invocation-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment` | body | `string` | no | Feedback comment. |
| `feedback_rating` | body | `string` | yes | Feedback rating. |
| `invocation_identifier` | path | `string` | yes | The AI invocation identifier. |

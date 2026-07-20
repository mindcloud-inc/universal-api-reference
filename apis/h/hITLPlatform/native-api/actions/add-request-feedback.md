# Add Request Feedback with HITL Platform

## Endpoint

- **Method:** `POST`
- **Path:** `/api/requests/:id/feedback`
- **Base URL:** `https://api.hitl.sh/v1`
- **Official documentation:** [Add Request Feedback](https://docs.hitl.sh/api-reference/requests/add-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedback.accuracy` | body | `number` | no | Accuracy rating from 1 to 5. |
| `feedback.category` | body | `string` | no | Feedback category such as positive, constructive, or issue. |
| `feedback.comment` | body | `string` | no | Free-form feedback comment. |
| `feedback.helpfulness` | body | `number` | no | Helpfulness rating from 1 to 5. |
| `feedback.rating` | body | `number` | no | Overall quality rating from 1 to 5. |
| `feedback.timeliness` | body | `number` | no | Timeliness rating from 1 to 5. |
| `id` | path | `string` | yes | The unique identifier of the completed request. |
| `would_recommend` | body | `boolean` | no | Whether you would recommend this reviewer for similar work. |

# Get Notification with Porsline

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/surveys/:survey_id/notifications/:pk/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Get Notification](https://developers.porsline.com/#tag/Notifications/paths/~1api~1v2~1surveys~1{survey_id}~1notifications~1{pk}~1/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `pk` | path | `number` | yes | Notification ID. |

# Auto Feedback Requests with GatherUp

Updates auto feedback request settings in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/auto-feedback-requests`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Auto Feedback Requests](https://app.gatherup.com/api/doc/business/auto-feedback-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | yes | Business id. |
| `autoFeedback` | body | `number` | yes | 1 = Automatic Mode \| 0 = Manual Mode |
| `autoSend` | body | `number` | no | Amount of feedbacks per day in Automatic Mode |

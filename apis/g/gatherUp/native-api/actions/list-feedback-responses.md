# List Feedback Responses with GatherUp

Retrieves a list of feedback responses from GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedbacks/responses/get`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [List Feedback Responses](https://app.gatherup.com/api/doc/feedbacks/responses/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | no | Business id (or multiple comma-separated ids.) |
| `feedbackId` | body | `number` | no | Feedback id (or multiple comma-separated ids.) |
| `from` | body | `string` | no | Received from |
| `page` | body | `number` | no | Page |
| `to` | body | `string` | no | Received to |

# Get Feedbacks Received with GatherUp

Retrieves received customer feedback from GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedbacks/get`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Get Feedbacks Received](https://app.gatherup.com/api/doc/feedbacks/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | no | Business id (or multiple comma-separated ids.) |
| `from` | body | `string` | no | Received from |
| `to` | body | `string` | no | Received to |
| `page` | body | `number` | no | Page |
| `minRecommend` | body | `number` | no | Minimal recommend |
| `maxRecommend` | body | `number` | no | Maximal recommend |
| `showSurvey` | body | `number` | no | Include Survey Question results |
| `customerId` | body | `number` | no | Return feedbacks only for a specific customer |
| `visible` | body | `number` | no | Return feedbacks visible or not |

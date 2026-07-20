# Send Customer Feedback Request with GatherUp

Creates a customer feedback request in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer/feedback/send`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Send Customer Feedback Request](https://app.gatherup.com/api/doc/customer/feedback/send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | body | `number` | yes | Customer id. |
| `ratingRevision` | body | `number` | no | 1 will send rating revision instead of new feedback request. 0 will create new feedback request. Default value is 1. |
| `checkThreshold` | body | `number` | no | 1 will check if threshold is reached If yes then it throws error. Default value is 0. |
| `jobId` | body | `string` | no | Sets JobID for repeat feedback request. Replaces existing JobID if rating revision. |

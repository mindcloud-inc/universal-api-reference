# List Online Reviews Received with GatherUp

Retrieves a list of online reviews from GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/online-reviews/get`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [List Online Reviews Received](https://app.gatherup.com/api/doc/online-reviews/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | no | Business id (or multiple comma-separated ids.) |
| `from` | body | `string` | no | Received from |
| `page` | body | `number` | no | Page |
| `to` | body | `string` | no | Received to |
| `type[]` | body | `array<string>` | no | Review type |
| `visible` | body | `number` | no | Show reviews which are visible or not |

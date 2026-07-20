# List Customers with GatherUp

Retrieves a list of customers from GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/get`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [List Customers](https://app.gatherup.com/api/doc/customers/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | no | Business ID (or multiple comma-separated ids.) |
| `customerId` | body | `number` | no | Customer ID |
| `customId` | body | `string` | no | Custom ID |
| `jobId` | body | `string` | no | Job ID |
| `email` | body | `string` | no | Customer email address. |
| `page` | body | `number` | no | Page. |
| `subscription` | body | `number` | no | Subscription of customer. |
| `showHistory` | body | `number` | no | Show all related feedbacks. |

# Update Customer Feedback with GatherUp

Updates existing customer feedback in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer/feedback/update`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Update Customer Feedback](https://app.gatherup.com/api/doc/customer/feedback/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerCustomId` | body | `string` | no | Customer custom id. |
| `customerId` | body | `number` | yes | Customer id. |
| `customerJobId` | body | `string` | no | Customer job id. |

# Get Scheduled Transaction with YNAB

Retrieves a scheduled transaction from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/scheduled_transactions/:scheduledTransactionId`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [Get Scheduled Transaction](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
| `scheduledTransactionId` | path | `string` | yes | The id of the scheduled transaction. |

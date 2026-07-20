# List Billing Account Users with ActivityInfo

Retrieves users for an ActivityInfo billing account.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/billingAccounts/:accountId/users`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [List Billing Account Users](https://www.activityinfo.org/support/docs/api/reference/getBillingAccountUsers.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | ActivityInfo billing account ID. |

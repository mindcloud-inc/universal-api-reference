# List Billing Account Databases with ActivityInfo

Retrieves databases for an ActivityInfo billing account.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/billingAccounts/:accountId/databases`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [List Billing Account Databases](https://www.activityinfo.org/support/docs/api/reference/getBillingAccountDatabases.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | ActivityInfo billing account ID. |

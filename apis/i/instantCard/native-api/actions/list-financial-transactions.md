# List Financial Transactions with InstantCard

Retrieves all financial transactions from InstantCard.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/financial_transactions`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [List Financial Transactions](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |

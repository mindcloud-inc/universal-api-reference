# Add Credit To Account with Billforward

Creates a new credit note for a Billforward account.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/credit`
- **Base URL:** `https://app-sandbox.billforward.net/v1`
- **Official documentation:** [Add Credit To Account](https://app.billforward.net/#/api/method/accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | The Billforward account ID to credit. |
| `description` | body | `string` | yes | Credit note description. |
| `value` | body | `number` | yes | Credit note value. |
| `currency` | body | `string` | yes | Credit note currency code. |

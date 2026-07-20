# Transfer Credits with BulkSMS

Transfers credits to another BulkSMS account.

## Endpoint

- **Method:** `POST`
- **Path:** `/credit/transfer`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [Transfer Credits](https://www.bulksms.com/developer/json/v1/#tag/credits/POST/credit/transfer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `toUsername` | body | `string` | yes | Username of the BulkSMS account that will receive credits. |
| `toUserId` | body | `number` | yes | Numeric user ID of the account that will receive credits. It must match the username. |
| `credits` | body | `number` | yes | Amount of credits to transfer. |
| `commentOnFrom` | body | `string` | no | Optional note shown on the sender account credit history. Maximum length: 100. |
| `commentOnTo` | body | `string` | no | Optional note shown on the recipient account credit history. Maximum length: 100. |

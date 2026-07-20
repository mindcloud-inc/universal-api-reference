# Create Bank Account with PostGrid Print & Mail

Creates a bank account in PostGrid Print & Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/bank_accounts`
- **Base URL:** `https://api.postgrid.com/print-mail/v1`
- **Official documentation:** [Create Bank Account](https://postgrid.readme.io/reference/bankaccounts_create-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bankName` | body | `string` | yes | The name of the bank. |
| `bankCountryCode` | body | `string` | yes | The bank country code. |
| `accountNumber` | body | `string` | yes | The bank account number. |
| `signatureText` | body | `string` | no | The signature text to print on cheques. |
| `signatureImage` | body | `string` | no | The signature image source to print on cheques. |
| `routingNumber` | body | `string` | no | The US routing number. |
| `transitNumber` | body | `string` | no | The Canadian transit number. |
| `routeNumber` | body | `string` | no | The Canadian route number. |
| `caDesignationNumber` | body | `string` | no | The Canadian designation number. |
| `bankPrimaryLine` | body | `string` | no | The primary address line for the bank. |
| `bankSecondaryLine` | body | `string` | no | The secondary address line for the bank. |
| `description` | body | `string` | no | An optional description visible in the API and dashboard. |
| `metadata` | body | `object` | no | Custom metadata for this bank account. |

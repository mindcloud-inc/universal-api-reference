# List Supported Beneficiary Banks with Airwallex

Retrieves supported beneficiary banks from Airwallex.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/beneficiary_form_schemas/supported_financial_institutions`
- **Base URL:** `https://api-demo.airwallex.com`
- **Official documentation:** [List Supported Beneficiary Banks](https://www.airwallex.com/docs/payouts/beneficiaries/retrieve-supported-beneficiary-banks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bank_country_code` | query | `string` | yes | The beneficiary bank country code, such as US. |
| `keyword` | query | `string` | no | Search keyword for supported financial institutions, minimum 3 characters. |
| `account_currency` | query | `string` | yes | The beneficiary account currency, such as USD. |
| `transfer_method` | query | `string` | yes | The payout transfer method, such as LOCAL or SWIFT. |
| `entity_type` | query | `string` | yes | The beneficiary entity type, such as PERSONAL or COMPANY. |
| `local_clearing_system` | query | `string` | no | Optional local clearing system, such as ACH. |

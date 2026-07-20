# Validate IBAN with Data8

Validates a submitted IBAN with Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/BankAccountValidation/IBANIsValid.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Validate IBAN](https://docs.data-8.co.uk/web-services/bankaccountvalidation/ibanisvalid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bic` | body | `string` | no | The optional BIC to validate. |
| `iban` | body | `string` | no | The optional IBAN to validate. |
| `options` | body | `object` | no | Optional settings that control bank validation behavior. |

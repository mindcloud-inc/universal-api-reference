# Validate IBAN with Abstract IBAN Validator

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/`
- **Base URL:** `https://ibanvalidation.abstractapi.com`
- **Official documentation:** [Validate IBAN](https://docs.abstractapi.com/api/iban-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `iban` | query | `string` | yes | International Bank Account Number to validate. Abstract accepts whitespace in the IBAN value. |

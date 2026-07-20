# Batch Validate Emails with Loqate

Validates multiple email addresses with Loqate.

## Endpoint

- **Method:** `GET`
- **Path:** `/EmailValidation/Batch/Validate/v1.20/json6.ws`
- **Base URL:** `https://api.addressy.com`
- **Official documentation:** [Batch Validate Emails](https://docs.loqate.com/api-reference/email-validation/batch-validate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Emails` | query | `string` | yes | Comma-separated email addresses to verify. |

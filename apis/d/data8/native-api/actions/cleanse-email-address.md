# Cleanse Email Address with Data8

Cleanses an email address with Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/EmailValidation/Cleanse.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Cleanse Email Address](https://docs.data-8.co.uk/web-services/emailvalidation/cleanse)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to validate. |
| `level` | body | `string` | yes | The validation level to apply. |
| `record` | body | `object` | no | Optional supporting identity data used to enrich email cleansing results. |
| `options` | body | `object` | no | Optional settings that control email validation behavior. |

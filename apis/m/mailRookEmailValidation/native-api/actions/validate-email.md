# Validate Email with MailRook Email Validation

Validates an email address in MailRook.

## Endpoint

- **Method:** `GET`
- **Path:** `/validate/:email`
- **Base URL:** `https://api.mailrook.com/v1`
- **Official documentation:** [Validate Email](https://mailrook.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Email address to validate. |
| `include` | query | `string` | no | Comma-separated enrichment data to include, such as risk or providers. |

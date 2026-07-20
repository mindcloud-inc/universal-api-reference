# List Email Validation Lists with turboSMTP

Retrieves email validation lists from turboSMTP.

## Endpoint

- **Method:** `GET`
- **Path:** `/emailvalidation/lists`
- **Base URL:** `https://pro.api.serversmtp.com/api/v2`
- **Official documentation:** [List Email Validation Lists](https://serversmtp.com/turbo-api/#/email-validator/getEmailValidationLists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Start date in YYYY-MM-DD format. |
| `to` | query | `string` | yes | End date in YYYY-MM-DD format. |

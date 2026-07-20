# Find Emails By Name And Domain with Anyleads

Finds emails in Anyleads by name and domain.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/find-emails-first-last`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Find Emails By Name And Domain](https://docs.anyleads.com/product/en/find-emails-from-first-name-last-name-and-company-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Company domain to use when generating the likely email. |
| `first_name` | body | `string` | yes | Lead first name. |
| `last_name` | body | `string` | yes | Lead last name. |

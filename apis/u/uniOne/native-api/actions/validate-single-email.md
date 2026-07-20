# Validate Single Email with UniOne

Validates a single email address in UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `email-validation/single.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Validate Single Email](https://docs.unione.io/en/web-api-ref#email-validation-single)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to validate. |

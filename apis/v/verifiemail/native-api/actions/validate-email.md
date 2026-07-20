# Validate Email with verifi.email

Validate a single email address and return deliverability checks, including syntax, MX, spoofing, and disposable-provider details.

## Endpoint

- **Method:** `GET`
- **Path:** `/check`
- **Base URL:** `https://api.verifi.email`
- **Official documentation:** [Validate Email](https://verifi.email/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to validate. |

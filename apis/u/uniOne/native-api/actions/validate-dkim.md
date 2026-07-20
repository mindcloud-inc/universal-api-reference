# Validate DKIM with UniOne

Validates DKIM records for a domain in UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `domain/validate-dkim.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Validate DKIM](https://docs.unione.io/en/web-api-ref#domain-validate-dkim)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Domain name to validate. |

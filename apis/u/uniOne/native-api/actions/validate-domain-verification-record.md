# Validate Domain Verification Record with UniOne

Validates a domain verification record in UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `domain/validate-verification-record.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Validate Domain Verification Record](https://docs.unione.io/en/web-api-ref#domain-validate-verification-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Domain name to validate. |

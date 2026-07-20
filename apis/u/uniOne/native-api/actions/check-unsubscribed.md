# Check Unsubscribed with UniOne

Checks whether an email address is unsubscribed in UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `unsubscribed/check.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Check Unsubscribed](https://docs.unione.io/en/web-api-ref#unsubscribed-check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Email address to check in the unsubscribed list. |

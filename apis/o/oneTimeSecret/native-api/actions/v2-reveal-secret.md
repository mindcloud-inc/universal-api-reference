# Reveal Secret with One-Time Secret

Reveals and consumes a secret from One-Time Secret by identifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/secret/:identifier/reveal`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Reveal Secret](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_secret_revealsecret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Secret identifier to reveal. |

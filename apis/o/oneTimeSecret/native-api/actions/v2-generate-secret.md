# Generate Secret with One-Time Secret

Creates a new secret with a generated value in One-Time Secret.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/secret/generate`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Generate Secret](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_generatesecret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `secret.share_domain` | body | `string` | yes | Domain used for generated share URLs. |

# V1 Test idempotency with Atlar

Tests idempotency in Atlar v1.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/idempotency-test`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [V1 Test idempotency](https://docs.atlar.com/v1/reference/post_v1-idempotency-test)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status` | query | `number` | no |
| `sleep` | query | `number` | no |

# Update Restrictions with Channex

Updates rate plan restrictions in Channex.

## Endpoint

- **Method:** `POST`
- **Path:** `/restrictions`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Update Restrictions](https://docs.channex.io/api-v.1-documentation/ari#update-rate-and-restrictions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `values[]` | body | `array<object>` | yes | Array of restriction update objects documented by Channex. |

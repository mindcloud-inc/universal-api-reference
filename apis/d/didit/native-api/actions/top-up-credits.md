# Top Up Credits with Didit

Creates a credit top-up request in Didit.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing/top-up/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Top Up Credits](https://docs.didit.me/management-api/billing/top-up)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount_in_dollars` | body | `number` | yes |
| `cancel_url` | body | `string` | no |
| `success_url` | body | `string` | no |

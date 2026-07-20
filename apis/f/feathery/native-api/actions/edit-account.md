# Edit Account with Feathery

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/account/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [Edit Account](https://api-docs.feathery.io/#edit-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accounts[]` | body | `array<object>` | yes | An array of account update objects. Each object can include email or account_id plus the fields to update. |

# Remove Account with Feathery

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/account/uninvite/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [Remove Account](https://api-docs.feathery.io/#remove-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accounts[]` | body | `array<object>` | yes | An array of account removal objects. Each object should include email or account_id per the Feathery docs. |

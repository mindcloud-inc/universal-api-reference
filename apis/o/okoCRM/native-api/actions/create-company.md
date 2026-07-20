# Create company with OkoCRM

Creates a new company in OkoCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Create company](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[][email]` | body | `string` | no | One email address to attach to the company. |
| `name` | body | `string` | yes | Company name. |
| `phones[][phone]` | body | `string` | no | One phone number to attach to the company. |

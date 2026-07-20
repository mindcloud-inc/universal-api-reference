# Create Customer with Housecall Pro

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Create Customer](https://docs.housecallpro.com/docs/housecall-public-api/4e0bf8c4d65d7-create-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `notifications_enabled` | body | `boolean` | no | — |
| `mobile_number` | body | `string` | no | — |
| `home_number` | body | `string` | no | — |
| `work_number` | body | `string` | no | — |
| `tags[]` | body | `array<string>` | no | Send multiple values as a array. |
| `lead_source` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
| `addresses[]` | body | `array<object>` | no | — |

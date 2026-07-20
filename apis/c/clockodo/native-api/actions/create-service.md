# Create Service with Clockodo

Creates a service in your Clockodo account.

## Endpoint

- **Method:** `POST`
- **Path:** `/services`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [Create Service](https://www.clockodo.com/en/api/services/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | body | `boolean` | no |
| `name` | body | `string` | yes |
| `note` | body | `string` | no |
| `number` | body | `string` | no |

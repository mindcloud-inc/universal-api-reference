# Create Organization with WEEEK

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/organizations`
- **Base URL:** `https://api.weeek.net/public/v1`
- **Official documentation:** [Create Organization](https://developers.weeek.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addresses[]` | body | `array<string>` | no | Optional addresses for the organization. Send multiple values as a array. |
| `emails[]` | body | `array<string>` | no | Optional email addresses for the organization. Send multiple values as a array. |
| `name` | body | `string` | yes | The organization name. |
| `phones[]` | body | `array<string>` | no | Optional phone numbers for the organization. Send multiple values as a array. |

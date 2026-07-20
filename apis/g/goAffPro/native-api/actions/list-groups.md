# List Groups with GoAffPro

Retrieves configured affiliate groups from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/groups`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Groups](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[]` | query | `array<string>` | yes | Fields to include in returned groups. |

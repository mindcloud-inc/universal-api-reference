# Sync Users with Softr

## Endpoint

- **Method:** `POST`
- **Path:** `https://studio-api.softr.io/v1/api/users/sync`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Sync Users](https://docs.softr.io/softr-api/api-setup-and-endpoints#sync-a-single-user-group-of-users-or-all-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | no | Target email addresses to sync. Leave blank to let Softr sync all users for the selected app domain. |

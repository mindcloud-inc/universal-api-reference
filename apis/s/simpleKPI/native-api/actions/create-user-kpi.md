# Create User KPI with SimpleKPI

Creates a KPI for a SimpleKPI user.

## Endpoint

- **Method:** `POST`
- **Path:** `users/:userId/kpis`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Create User KPI](https://support.simplekpi.com/Developers/UsersKPIs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | no | The KPI ID to assign to the user. |
| `sort_order` | body | `number` | no | The display order of the KPI for the user. |
| `user_target` | body | `number` | no | An optional target override for the assigned KPI. |
| `userId` | path | `number` | no | The user ID. |

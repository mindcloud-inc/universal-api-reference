# Update User KPI with SimpleKPI

Updates a KPI for a SimpleKPI user.

## Endpoint

- **Method:** `PUT`
- **Path:** `users/:userId/kpis/:id`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Update User KPI](https://support.simplekpi.com/Developers/UsersKPIs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | no | The KPI ID assigned to the user. |
| `sort_order` | body | `number` | no | The display order of the KPI for the user. |
| `user_target` | body | `number` | no | An optional target override for the assigned KPI. |
| `userId` | path | `number` | no | The user ID. |

# Delete User KPI with SimpleKPI

Deletes a KPI from a SimpleKPI user.

## Endpoint

- **Method:** `DELETE`
- **Path:** `users/:userId/kpis/:id`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Delete User KPI](https://support.simplekpi.com/Developers/UsersKPIs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | no | The KPI ID assigned to the user. |
| `userId` | path | `number` | no | The user ID. |

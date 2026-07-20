# Get User KPI with SimpleKPI

Retrieves a KPI assigned to a SimpleKPI user.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:userId/kpis/:id`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Get User KPI](https://support.simplekpi.com/Developers/UsersKPIs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | no | The KPI ID assigned to the user. |
| `userId` | path | `number` | no | The user ID. |

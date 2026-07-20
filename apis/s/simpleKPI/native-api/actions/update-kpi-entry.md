# Update KPI Entry with SimpleKPI

Updates an existing KPI entry in SimpleKPI.

## Endpoint

- **Method:** `PUT`
- **Path:** `kpientries/:id`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Update KPI Entry](https://support.simplekpi.com/Developers/KPIEntries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actual` | body | `number` | no | The KPI actual value. |
| `addToActual` | body | `boolean` | no | Whether to add to the existing actual value. |
| `email` | body | `string` | no | The user email for the entry when user_id is not used. |
| `entry_date` | body | `string` | no | The KPI entry date in YYYY-MM-DD format. |
| `id` | path | `number` | no | The KPI entry ID. |
| `kpi_id` | body | `number` | no | The SimpleKPI KPI ID for the entry. |
| `notes` | body | `string` | no | Optional notes for the KPI entry. |
| `setActual` | body | `boolean` | no | Whether to set the actual value. |
| `setNotes` | body | `boolean` | no | Whether to set the notes value. |
| `setTarget` | body | `boolean` | no | Whether to set the target value. |
| `target` | body | `number` | no | The KPI target value. |
| `user_id` | body | `number` | no | The SimpleKPI user ID for the entry. |

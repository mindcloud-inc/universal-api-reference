# Update KPI with SimpleKPI

Updates an existing KPI in SimpleKPI.

## Endpoint

- **Method:** `PUT`
- **Path:** `kpis/:id`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Update KPI](https://support.simplekpi.com/Developers/KPIs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aggregate_function` | body | `string` | no | The KPI aggregate function: AVG or SUM. |
| `category_id` | body | `number` | no | The SimpleKPI category ID to assign to the KPI. |
| `description` | body | `string` | no | The KPI description. |
| `frequency_id` | body | `string` | no | The SimpleKPI frequency ID to assign to the KPI. |
| `icon_id` | body | `number` | no | The SimpleKPI icon ID to assign to the KPI. |
| `id` | path | `number` | no | The KPI ID. |
| `is_active` | body | `boolean` | no | Whether the KPI is active. |
| `name` | body | `string` | no | The KPI name. |
| `sort_order` | body | `number` | no | The display sort order for the KPI. |
| `target_default` | body | `number` | no | The default KPI target value. |
| `unit_id` | body | `number` | no | The SimpleKPI unit ID to assign to the KPI. |
| `value_direction` | body | `string` | no | The KPI value direction: U, D, or N. |

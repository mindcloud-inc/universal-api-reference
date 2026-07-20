# Update Maintenance Window with Pingdom

## Endpoint

- **Method:** `PUT`
- **Path:** `/maintenance/:id`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [Update Maintenance Window](https://docs.pingdom.com/api/#tag/Maintenance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Identifier of the maintenance window. |
| `description` | body | `string` | no | Maintenance window description. |
| `from` | body | `number` | no | Initial maintenance start as UNIX time. |
| `to` | body | `number` | no | Initial maintenance end as UNIX time. |
| `recurrencetype` | body | `string` | no | Recurrence type. |
| `repeatevery` | body | `number` | no | Repeat every n-th interval. |
| `effectiveto` | body | `number` | no | Recurrence end as UNIX time. |
| `uptimeids[]` | body | `array<number>` | no | Uptime checks assigned to the maintenance window. |
| `tmsids[]` | body | `array<number>` | no | Transaction checks assigned to the maintenance window. |

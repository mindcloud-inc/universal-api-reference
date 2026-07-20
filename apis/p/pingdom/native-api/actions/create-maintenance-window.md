# Create Maintenance Window with Pingdom

## Endpoint

- **Method:** `POST`
- **Path:** `/maintenance`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [Create Maintenance Window](https://docs.pingdom.com/api/#tag/Maintenance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | Maintenance window description. |
| `from` | body | `number` | yes | Initial maintenance start as UNIX time. |
| `to` | body | `number` | yes | Initial maintenance end as UNIX time. |
| `recurrencetype` | body | `string` | no | Recurrence type. |
| `repeatevery` | body | `number` | no | Repeat every n-th interval. |
| `effectiveto` | body | `number` | no | Recurrence end as UNIX time. |
| `uptimeids[]` | body | `array<number>` | no | Uptime checks assigned to the maintenance window. |
| `tmsids[]` | body | `array<number>` | no | Transaction checks assigned to the maintenance window. |

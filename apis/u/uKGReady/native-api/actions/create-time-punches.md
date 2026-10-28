# Create Time Punches with UKG Ready

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/companies/:cid/time-punches/collection`
- **Base URL:** `https://{hostname}/ta/rest`
- **Official documentation:** [Create Time Punches](https://secure7.saashr.com/ta/docs/rest/public)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cid` | path | `string` | no |
| `punches[].cost_centers[].index` | body | `number` | no |
| `punches[].cost_centers[].value.id` | body | `number` | no |
| `punches[].employee` | body | `object` | no |
| `punches[].employee.account_id` | body | `number` | no |
| `punches[]` | body | `array<object>` | no |
| `punches[].cost_centers[].value` | body | `object` | no |
| `punches[].employee.badge_id` | body | `string` | no |
| `punches[].ip` | body | `string` | no |
| `punches[].timestamp` | body | `date` | yes |
| `punches[].timestamp_type` | body | `list<string>` | no |
| `punches[].raw_type` | body | `list<string>` | yes |
| `punches[].latitude` | body | `number` | no |
| `punches[].longitude` | body | `number` | no |
| `punches[].cost_centers[]` | body | `array<object>` | no |
| `punches[].device_id` | body | `string` | no |
| `punches[].terminal_id` | body | `number` | no |
| `punches[].status` | body | `number` | no |

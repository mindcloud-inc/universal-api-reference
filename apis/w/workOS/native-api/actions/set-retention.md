# Set Retention with WorkOS

Sets retention in your WorkOS environment.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/{id}/audit_logs_retention`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Set Retention](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the Organization. |
| `retention_period_in_days` | body | `number` | yes | The number of days Audit Log events will be retained. Valid values are `30` and `365`. |

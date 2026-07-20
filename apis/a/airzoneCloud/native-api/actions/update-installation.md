# Update Installation with Airzone Cloud

Updates all climate zones in an installation in Airzone Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/installations/{installationId}`
- **Base URL:** `https://m.airzonecloud.com/api/v1`
- **Official documentation:** [Update Installation](https://developers.airzonecloud.com/docs/web-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `installationId` | path | `string` | yes | The Airzone installation identifier. |
| `opts` | body | `object` | no | Optional object for extra settings, such as `units` when sending a setpoint. |
| `params` | body | `object` | yes | Object of installation-wide climate changes to apply, such as `power`, `mode`, `setpoint`, or `speed`. |

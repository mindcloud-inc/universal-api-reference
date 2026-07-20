# Update Installation Group with Airzone Cloud

Updates all devices in an installation group in Airzone Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/installations/{installationId}/group/{groupId}`
- **Base URL:** `https://m.airzonecloud.com/api/v1`
- **Official documentation:** [Update Installation Group](https://developers.airzonecloud.com/docs/web-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Airzone installation group identifier. |
| `installationId` | path | `string` | yes | The Airzone installation identifier. |
| `opts` | body | `object` | no | Optional object for extra settings, such as `units` when sending a setpoint. |
| `params` | body | `object` | yes | Object of group climate changes to apply, such as `power`, `mode`, `setpoint`, or `speed`. |

# Modify a scenario with xMatters

Updates a scenario in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `forms/{formId}/scenarios`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Modify a scenario](https://help.xmatters.com/xmapi/index.html#modify-a-scenario)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `string` | no |
| `id` | body | `string` | no |
| `name` | body | `string` | no |
| `targetDeviceNames` | body | `list<string>` | no |

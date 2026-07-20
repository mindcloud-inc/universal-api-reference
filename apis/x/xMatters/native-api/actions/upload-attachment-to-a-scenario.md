# Upload attachment to a scenario with xMatters

Uploads attachment to a scenario to your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `forms/{formId}/scenarios/{scenarioId}/attachments`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Upload attachment to a scenario](https://help.xmatters.com/xmapi/index.html#upload-attachment-to-a-scenario)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `string` | no |
| `fileName` | body | `string` | no |
| `formId` | path | `string` | no |
| `scenarioId` | path | `string` | no |

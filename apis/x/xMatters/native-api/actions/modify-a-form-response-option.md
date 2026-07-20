# Modify a form response option with xMatters

Updates a form response option in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `forms/{formId}/response-options`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Modify a form response option](https://help.xmatters.com/xmapi/index.html#modify-a-form-response-option)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `action` | body | `string` | no |
| `allowComments` | body | `boolean` | no |
| `contribution` | body | `string` | no |
| `description` | body | `string` | no |
| `formId` | path | `string` | no |
| `id` | body | `string` | no |
| `joinConference` | body | `boolean` | no |
| `number` | body | `number` | no |
| `prompt` | body | `string` | no |
| `text` | body | `string` | no |

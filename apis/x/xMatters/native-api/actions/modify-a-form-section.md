# Modify a form section with xMatters

Updates a form section in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `forms/{formId}/sections`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Modify a form section](https://help.xmatters.com/xmapi/index.html#modify-a-form-section)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `bridgeType` | body | `string` | no |
| `collapsed` | body | `boolean` | no |
| `form` | body | `string` | no |
| `formId` | path | `string` | no |
| `id` | body | `string` | no |
| `orderNum` | body | `number` | no |
| `title` | body | `string` | no |
| `type` | body | `string` | no |
| `visible` | body | `boolean` | no |

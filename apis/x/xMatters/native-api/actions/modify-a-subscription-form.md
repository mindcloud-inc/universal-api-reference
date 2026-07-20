# Modify a subscription form with xMatters

Updates a subscription form in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `plans/{planId}/subscription-forms`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Modify a subscription form](https://help.xmatters.com/xmapi/index.html#modify-a-subscription-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `form` | body | `string` | no |
| `id` | body | `string` | no |
| `planId` | path | `string` | no |
| `propertyDefinitions` | body | `list<string>` | no |
| `scope` | body | `string` | no |
| `subscribeOthers` | body | `boolean` | no |

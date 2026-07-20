# Create a subscription form with xMatters

Creates a subscription form in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `plans/{planId}/subscription-forms`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Create a subscription form](https://help.xmatters.com/xmapi/index.html#create-a-subscription-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `devicesSectionCollapsed` | body | `boolean` | no |
| `devicesSectionVisible` | body | `boolean` | no |
| `name` | body | `string` | no |
| `notificationDelay` | body | `number` | no |
| `oneWay` | body | `boolean` | no |
| `planId` | path | `string` | no |
| `propertyDefinitions` | body | `list<string>` | no |
| `roles` | body | `list<string>` | no |
| `scope` | body | `string` | no |
| `subscribeOthers` | body | `boolean` | no |

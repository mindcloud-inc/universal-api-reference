# Create plan properties with xMatters

Creates plan properties in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `plans/{planId}/property-definitions`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Create plan properties](https://help.xmatters.com/xmapi/index.html#create-plan-properties)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `default` | body | `string` | no |
| `description` | body | `string` | no |
| `helpText` | body | `string` | no |
| `maxLength` | body | `number` | no |
| `minLength` | body | `number` | no |
| `name` | body | `string` | no |
| `pattern` | body | `string` | no |
| `planId` | path | `string` | no |
| `propertyType` | body | `string` | no |
| `validate` | body | `boolean` | no |

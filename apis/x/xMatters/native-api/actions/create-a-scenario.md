# Create a scenario with xMatters

Creates a scenario in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `forms/{formId}/scenarios`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Create a scenario](https://help.xmatters.com/xmapi/index.html#create-a-scenario)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `attachments` | body | `list<string>` | no |
| `bypassPhoneIntro` | body | `boolean` | no |
| `description` | body | `string` | no |
| `escalationOverride` | body | `boolean` | no |
| `expirationInMinutes` | body | `number` | no |
| `formId` | path | `string` | no |
| `name` | body | `string` | no |
| `overrideDeviceRestrictions` | body | `boolean` | no |
| `permitted` | body | `list<string>` | no |
| `priority` | body | `string` | no |
| `properties` | body | `string` | no |
| `recipients` | body | `list<string>` | no |
| `requirePhonePassword` | body | `boolean` | no |
| `senderOverrides` | body | `string` | no |
| `targetDeviceNames` | body | `list<string>` | no |

# Create a group with xMatters

Creates a group in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `groups`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Create a group](https://help.xmatters.com/xmapi/index.html#create-a-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `allowDuplicates` | body | `boolean` | no |
| `description` | body | `string` | no |
| `observedByAll` | body | `boolean` | no |
| `observers` | body | `list<string>` | no |
| `recipientType` | body | `string` | no |
| `site` | body | `string` | no |
| `status` | body | `string` | no |
| `supervisors` | body | `list<string>` | no |
| `targetName` | body | `string` | no |
| `useDefaultDevices` | body | `boolean` | no |

# Create a change record with xMatters

Creates a change record in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `changes`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Create a change record](https://help.xmatters.com/xmapi/index.html#create-a-change-record)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `changedAt` | body | `string` | no |
| `changedBy` | body | `string` | no |
| `changeType` | body | `string` | no |
| `service` | body | `string` | no |
| `source` | body | `string` | no |
| `summary` | body | `string` | no |

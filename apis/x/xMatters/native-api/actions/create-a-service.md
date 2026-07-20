# Create a service with xMatters

Creates a service in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `services`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Create a service](https://help.xmatters.com/xmapi/index.html#create-a-service)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `ownedBy` | body | `string` | no |
| `serviceTier` | body | `string` | no |
| `serviceType` | body | `string` | no |
| `targetName` | body | `string` | no |

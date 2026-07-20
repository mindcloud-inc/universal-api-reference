# Create Group with FileCloud

Creates a new group in FileCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/scim/Groups`
- **Base URL:** `https://mindcloud.filecloudtrial.com/api/v1`
- **Official documentation:** [Create Group](https://fcapi-v1.filecloud.com/#/scim/createScimGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | yes | Group display name. |
| `emailId` | body | `string` | no | Group email address. |

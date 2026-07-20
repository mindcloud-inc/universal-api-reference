# Get Resource Type by Name with FileCloud

Retrieves a resource type from FileCloud by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/scim/ResourceTypes/:name`
- **Base URL:** `https://mindcloud.filecloudtrial.com/api/v1`
- **Official documentation:** [Get Resource Type by Name](https://fcapi-v1.filecloud.com/#/scim/getResourceTypeByName)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Resource type name. Verified values include User and Group. |

# Update Resource with Makeplans

Updates an existing resource in Makeplans.

## Endpoint

- **Method:** `PUT`
- **Path:** `/resources/:resourceId`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Update Resource](https://developer.makeplans.com/endpoints/resources/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource.capacity` | body | `number` | no | Resource capacity. |
| `resource.title` | body | `string` | no | Resource title. |
| `resourceId` | path | `number` | yes | The Makeplans resource ID. |

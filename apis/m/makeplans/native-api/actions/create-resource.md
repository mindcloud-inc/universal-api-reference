# Create Resource with Makeplans

Creates a new resource in Makeplans.

## Endpoint

- **Method:** `POST`
- **Path:** `/resources`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Create Resource](https://developer.makeplans.com/endpoints/resources/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource.title` | body | `string` | yes | Resource title. |
| `resource.capacity` | body | `number` | no | Resource capacity. |

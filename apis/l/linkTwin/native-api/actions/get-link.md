# Get Link with LinkTwin

Retrieves a link from LinkTwin by ID or short URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/url/:id`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Get Link](https://linktw.in/developers#get-a-single-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Link ID or full short URL. |
| `timezone` | query | `string` | no | Timezone override for response dates. |

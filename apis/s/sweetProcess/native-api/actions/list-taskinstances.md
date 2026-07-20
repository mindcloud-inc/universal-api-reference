# List Taskinstances with SweetProcess

Retrieves task instances from SweetProcess.

## Endpoint

- **Method:** `GET`
- **Path:** `/taskinstances/`
- **Base URL:** `https://www.sweetprocess.com/api/v1`
- **Official documentation:** [List Taskinstances](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | query | `number` | no | Filter task instances belonging to the given task template. |
| `user` | query | `string` | no | Filter tasks assigned to the given user API URL. |
| `content_type` | query | `string` | no | Filter tasks for a specific document type such as procedure or process. |
| `object_id` | query | `number` | no | Filter tasks for the referenced document ID. |
| `completed` | query | `boolean` | no | Return only completed or incomplete task instances. |
| `due__gte` | query | `date` | no | Lower bound for due date filtering in ISO 8601 format. |
| `due__lte` | query | `date` | no | Upper bound for due date filtering in ISO 8601 format. |

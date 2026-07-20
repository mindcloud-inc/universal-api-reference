# List Project Users with CompanyCam

Retrieve a list of users assigned to a specified Project.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:id/assigned_users`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [List Project Users](https://docs.companycam.com/reference/listprojectassignedusers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the Project |

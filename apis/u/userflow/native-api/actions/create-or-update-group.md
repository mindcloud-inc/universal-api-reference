# Create Or Update Group with Userflow

Creates or updates a group in Userflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [Create Or Update Group](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Unique identifier for the group. |
| `attributes` | body | `object` | no | Group attributes to merge into the Userflow group. |

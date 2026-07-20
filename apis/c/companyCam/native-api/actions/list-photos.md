# List Photos with CompanyCam

Retrieves a list of photos from CompanyCam.

## Endpoint

- **Method:** `GET`
- **Path:** `photos`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [List Photos](https://docs.companycam.com/reference/listphotos)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_ids` | query | `number` | no | Include photos from one of these project IDs. Send multiple values as a array. |
| `start_date` | query | `date` | no | Timestamp to return photos captured on or after this value. |
| `end_date` | query | `date` | no | Timestamp to return photos captured on or before this value. |
| `user_ids` | query | `list<number>` | no | Include photos captured by one of these user IDs. Send multiple values as a array. |
| `group_ids` | query | `list<number>` | no | Include photos captured by users in one of these group IDs. Send multiple values as a array. |
| `tag_ids` | query | `list<number>` | no | Include photos with one of these tag IDs. Send multiple values as a array. |

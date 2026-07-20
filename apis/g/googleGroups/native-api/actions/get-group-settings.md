# Get Group Settings with Google Groups

Retrieves settings for a group in Google Groups.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.googleapis.com/groups/v1/groups/:groupUniqueId`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Get Group Settings](https://developers.google.com/workspace/admin/groups-settings/v1/reference/groups/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupUniqueId` | path | `string` | yes | The group email address used by the Groups Settings API. |

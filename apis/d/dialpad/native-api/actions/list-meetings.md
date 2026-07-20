# List Meetings with Dialpad

Retrieves meetings for a specific Dialpad user.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [List Meetings](https://developers.dialpad.com/reference/meetingslist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | query | `number` | yes | The Dialpad user's id. |
| `start_datetime` | query | `date` | yes | The meeting's start time (UTC seconds-since-epoch timestamp). |
| `end_datetime` | query | `date` | no | The meeting's end time (UTC seconds-since-epoch timestamp). |
| `cursor` | query | `string` | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |

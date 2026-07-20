# Get Meeting Type with Lemcal

Retrieves a meeting type from Lemcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetingTypes/:_id`
- **Base URL:** `https://api.lemcal.com/api/lemcal`
- **Official documentation:** [Get Meeting Type](https://developer.lemcal.com/#get-a-meeting-type)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | path | `string` | yes | The ID of the meeting type to retrieve. |

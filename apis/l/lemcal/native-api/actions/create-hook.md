# Create Hook with Lemcal

Creates a new hook in Lemcal.

## Endpoint

- **Method:** `POST`
- **Path:** `/hooks`
- **Base URL:** `https://api.lemcal.com/api/lemcal`
- **Official documentation:** [Create Hook](https://developer.lemcal.com/#create-a-hook)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetUrl` | body | `string` | yes | The callback URL for the hook. |
| `meetingTypeId` | body | `string` | no | A specific meeting type to associate with the hook. |
| `anyMeetingType` | body | `boolean` | no | Apply the hook to any meeting type. |

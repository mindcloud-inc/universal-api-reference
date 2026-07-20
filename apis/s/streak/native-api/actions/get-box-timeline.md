# Get Box Timeline with Streak

Retrieves timeline entries for a box in Streak.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/boxes/:boxKey/timeline`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Get Box Timeline](https://streak.readme.io/reference/get-timeline-for-a-box)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boxKey` | path | `string` | yes | The key of the box to get the timeline for. |
| `filters` | query | `list<string>` | no | The timeline entity types to include. Accepted values: `CALL_LOGS`, `COMMENTS`, `EMAILS`, `FILES`, `HANGOUTS_CHAT`, `MEETING_NOTES`, `NEWSFEED_BOX_CREATION_MOVE`, `NEWSFEED_BOX_EDIT`. Send multiple values as a array. |
| `direction` | query | `list<string>` | no | Whether to return results in ascending or descending timestamp order. Accepted values: `Ascending`, `Descending`. |
| `startTimestamp` | query | `number` | no | The timestamp boundary for returned results. |

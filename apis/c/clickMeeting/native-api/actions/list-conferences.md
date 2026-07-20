# List Conferences with ClickMeeting

Retrieves conferences from ClickMeeting by active or inactive status.

## Endpoint

- **Method:** `GET`
- **Path:** `conferences/{{status}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [List Conferences](https://dev.clickmeeting.com/api-doc/#get_conferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | path | `list` | yes | Choose whether to return active or inactive conference rooms. Accepted values: `active`, `inactive`. |
| `page` | query | `number` | no | Optional page number for inactive conference paging. |

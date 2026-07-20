# Add a comment to an event with xMatters

Adds a comment to an event in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `events/{eventId}/annotations`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Add a comment to an event](https://help.xmatters.com/xmapi/index.html#add-a-comment-to-an-event)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `comment` | body | `string` | no |
| `eventId` | path | `string` | no |

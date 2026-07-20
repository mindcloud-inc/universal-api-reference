# Get Event RSVP with Invision Community

## Endpoint

- **Method:** `GET`
- **Path:** `/calendar/events/:id/rsvps/:member_id`
- **Base URL:** `{communityBaseUrl}/api`
- **Official documentation:** [Get Event RSVP](https://invisioncommunity.com/developers/rest-api/index/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Event identifier. |
| `member_id` | path | `number` | yes | Member identifier. |

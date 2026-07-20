# Update Activity with Teamgate

Updates an activity in Teamgate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/{{eventId}}`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Update Activity](https://developers.teamgate.com/#5fecc71a-e467-4272-bed4-dc2b5b8e0341)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Unique key of the activity. |
| `name` | body | `string` | no | Updated activity name. |

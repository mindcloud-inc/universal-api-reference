# Track User Event with Engage

Tracks a user event in Engage.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:uid/events`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Track User Event](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#track-user-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | The event title. |
| `properties` | body | `object` | no | Additional event properties as an object. |
| `timestamp` | body | `string` | no | Timestamp of the event. |
| `uid` | path | `string` | yes | The user ID from your application. |
| `value` | body | `string` | no | The event value. |

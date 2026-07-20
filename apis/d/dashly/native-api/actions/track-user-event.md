# Track User Event with Dashly

Tracks an event for a Dashly user.

## Endpoint

- **Method:** `POST`
- **Path:** `users/:id/events`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Track User Event](https://developers.dashly.io/webapi/endpoints/users/events/post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by_user_id` | query | `boolean` | no | — |
| `event` | body | `string` | yes | — |
| `id_as_string` | query | `boolean` | no | — |
| `params` | body | `string` | no | JSON object string with event properties, for example {"item":"chicken"}. |
| `created` | body | `number` | no | — |

# Update Subscriber Status with Engage

Updates a user's subscription status for an Engage list.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:id/subscribers/:uid`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Update Subscriber Status](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#update-subscriber-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Engage list ID. |
| `subscribed` | body | `boolean` | yes | Set to true to subscribe or false to unsubscribe the user. |
| `uid` | path | `string` | yes | The subscriber user ID from your application. |

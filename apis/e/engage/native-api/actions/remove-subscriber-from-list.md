# Remove Subscriber from List with Engage

Removes a subscriber from an Engage list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/:id/subscribers/:uid`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Remove Subscriber from List](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#remove-a-subscriber-from-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Engage list ID. |
| `uid` | path | `string` | yes | The subscriber user ID from your application. |

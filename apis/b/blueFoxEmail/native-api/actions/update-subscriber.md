# Update Subscriber with BlueFox Email

Updates a subscriber in a BlueFox Email list.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/subscriber-lists/:subscriberListId/:subscriberEmailAddress`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Update Subscriber](https://bluefox.email/docs/api/subscriber-list-management#update-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriberListId` | path | `string` | yes | BlueFox subscriber list ID. |
| `subscriberEmailAddress` | path | `string` | yes | Email address of the subscriber to update. |
| `email` | body | `string` | no | Updated subscriber email address. |
| `name` | body | `string` | no | Updated subscriber name. |

# Get Subscriber with BlueFox Email

Retrieves a subscriber from a BlueFox Email list.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/subscriber-lists/:subscriberListId/:subscriberEmailAddress`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Get Subscriber](https://bluefox.email/docs/api/subscriber-list-management#get-one-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriberListId` | path | `string` | yes | BlueFox subscriber list ID. |
| `subscriberEmailAddress` | path | `string` | yes | Email address of the subscriber to retrieve. |

# Pause Subscription with BlueFox Email

Pauses a subscriber in a BlueFox Email list.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/subscriber-lists/:subscriberListId/:subscriberEmailAddress`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Pause Subscription](https://bluefox.email/docs/api/subscriber-list-management#pause-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriberListId` | path | `string` | yes | BlueFox subscriber list ID. |
| `subscriberEmailAddress` | path | `string` | yes | Email address of the subscriber to pause. |
| `pausedUntil` | body | `string` | yes | ISO date string for how long the subscriber stays paused. |

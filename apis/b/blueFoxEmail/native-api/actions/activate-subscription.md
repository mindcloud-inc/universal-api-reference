# Activate Subscription with BlueFox Email

Activates a subscriber in a BlueFox Email list.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/subscriber-lists/:subscriberListId/:subscriberEmailAddress`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Activate Subscription](https://bluefox.email/docs/api/subscriber-list-management#activate-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriberListId` | path | `string` | yes | BlueFox subscriber list ID. |
| `subscriberEmailAddress` | path | `string` | yes | Email address of the subscriber to activate. |

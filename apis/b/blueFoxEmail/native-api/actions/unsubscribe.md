# Unsubscribe with BlueFox Email

Unsubscribes a contact from a BlueFox Email list.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/subscriber-lists/:subscriberListId/:subscriberEmailAddress`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Unsubscribe](https://bluefox.email/docs/api/subscriber-list-management#unsubscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriberListId` | path | `string` | yes | BlueFox subscriber list ID. |
| `subscriberEmailAddress` | path | `string` | yes | Email address of the subscriber to unsubscribe. |

# Subscribe with BlueFox Email

Subscribes a contact to a BlueFox Email list.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscriber-lists/:subscriberListId`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Subscribe](https://bluefox.email/docs/api/subscriber-list-management#subscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriberListId` | path | `string` | yes | BlueFox subscriber list ID. |
| `email` | body | `string` | yes | Email address to subscribe. |
| `name` | body | `string` | no | Name of the subscriber. |

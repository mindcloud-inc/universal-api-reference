# List Subscriber Events with Sender

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:subscriberKey/events`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [List Subscriber Events](https://api.sender.net/subscribers/events/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriberKey` | path | `string` | yes | Subscriber email address, phone number, or ID. |
| `actions` | query | `string<string>` | yes | JSON array string of one or more event action types: opened, bounced, clicked, unsubscribed, or got. |

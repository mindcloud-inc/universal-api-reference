# Unsubscribe Subscriber with Mailcoach

Unsubscribes an existing subscriber in Mailcoach.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/:uuid/unsubscribe`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [Unsubscribe Subscriber](https://www.mailcoach.app/api-documentation/endpoints/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | The UUID of the subscriber to unsubscribe. |

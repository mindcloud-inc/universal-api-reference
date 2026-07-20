# Confirm Subscriber with Mailcoach

Confirms an existing subscriber in Mailcoach.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/:uuid/confirm`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [Confirm Subscriber](https://www.mailcoach.app/api-documentation/endpoints/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | The UUID of the subscriber to confirm. |

# Add Tags To Subscriber with Mailcoach

Adds tags to a subscriber in Mailcoach.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/:uuid/tags`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [Add Tags To Subscriber](https://www.mailcoach.app/api-documentation/endpoints/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags[]` | body | `array<string>` | yes | The tags to add. |
| `uuid` | path | `string` | yes | The UUID of the subscriber whose tags should be added. |

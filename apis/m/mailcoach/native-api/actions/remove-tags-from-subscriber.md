# Remove Tags From Subscriber with Mailcoach

Removes tags from a subscriber in Mailcoach.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/subscribers/:uuid/tags`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [Remove Tags From Subscriber](https://www.mailcoach.app/api-documentation/endpoints/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags[]` | body | `array<string>` | yes | The tags to remove. |
| `uuid` | path | `string` | yes | The UUID of the subscriber whose tags should be removed. |

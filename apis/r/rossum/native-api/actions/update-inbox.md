# Update Inbox with Rossum

Updates an inbox in Rossum.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inboxes/:inboxID`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Update Inbox](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboxID` | path | `number` | yes | Rossum inbox ID. |
| `name` | body | `string` | no | Updated inbox name. |
| `queue` | body | `string` | no | Inbox queue URL. |
| `queues` | body | `list<string>` | no | Inbox queue URLs. |

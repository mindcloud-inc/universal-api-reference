# Create Group with Schedule It

Creates a new group in Schedule It.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups`
- **Base URL:** `https://www.scheduleit.com/api`
- **Official documentation:** [Create Group](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The group name. |
| `color_back` | body | `string` | no | The group background color. |
| `positionv` | body | `string` | no | The group vertical position. |
| `min_resources` | body | `string` | no | The minimum resources setting. |
| `max_resources` | body | `string` | no | The maximum resources setting. |
| `hide_from_main` | body | `string` | no | Whether the group is hidden from the main screen. |
| `hide_from_event` | body | `string` | no | Whether the group is hidden from the event screen. |

# Add Subscriber to Group with Sender

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/groups/:groupId`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [Add Subscriber to Group](https://api.sender.net/subscribers/add-group/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Provide the group id. |
| `subscribers[]` | body | `array<string>` | yes | Array of email addresses that would be added to this group. |
| `conditions` | body | `string` | no | Select subscribers in bulk. Cannot be combined with subscribers. |
| `trigger_automation` | body | `boolean` | no | Send false to avoid activating an automation. |

# Remove Subscriber from Group with Sender

## Endpoint

- **Method:** `DELETE`
- **Path:** `/subscribers/groups/:groupId`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [Remove Subscriber from Group](https://api.sender.net/subscribers/remove-group/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Provide the group id. |
| `subscribers[]` | body | `array<string>` | yes | Array of email addresses that would be removed from this group. |
| `conditions` | body | `string` | no | Select subscribers in bulk. Cannot be combined with subscribers. |

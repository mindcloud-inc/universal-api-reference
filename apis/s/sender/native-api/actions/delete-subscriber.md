# Delete Subscriber with Sender

## Endpoint

- **Method:** `DELETE`
- **Path:** `/subscribers`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [Delete Subscriber](https://api.sender.net/subscribers/delete-subscriber/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscribers[]` | body | `array<string>` | yes | Array of subscriber emails to be deleted. |
| `conditions` | body | `string` | no | Select subscribers in bulk. Cannot be combined with subscribers. |

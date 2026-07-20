# Update Subscriber with Laposta

Updates an existing subscriber in Laposta.

## Endpoint

- **Method:** `POST`
- **Path:** `/member/:memberId`
- **Base URL:** `https://api.laposta.nl/v2`
- **Official documentation:** [Update Subscriber](https://api.laposta.nl/doc/index.en.php#members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberId` | path | `string` | yes | The subscriber ID or email address to update. |
| `list_id` | body | `string` | yes | The ID of the list that owns the subscriber. |
| `email` | body | `string` | no | Updated subscriber email address. |
| `state` | body | `list` | no | Updated subscriber state. Accepted values: `active`, `unsubscribed`. |

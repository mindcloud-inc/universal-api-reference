# Cancel Emergency Receipts by Tag with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/receipts/cancel_by_tag/:tag.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Cancel Emergency Receipts by Tag](https://pushover.net/api/receipts#cancel_by_tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | path | `string` | yes | Tag used to cancel active emergency-priority messages. |

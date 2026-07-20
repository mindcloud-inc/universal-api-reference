# Send Message To Inbox with CueGrowth

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/{inbox_id}/send`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [Send Message To Inbox](https://cuegrowth.ai/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | ID of the inbox. |
| `message` | body | `string` | no | Message to send to the inbox. |

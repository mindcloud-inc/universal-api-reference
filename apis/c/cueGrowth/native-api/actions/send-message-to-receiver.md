# Send Message To Receiver with CueGrowth

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/send_message_to_receiver`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [Send Message To Receiver](https://cuegrowth.ai/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_email` | body | `string` | yes | Email of the user. |
| `receiver_username` | body | `string` | yes | LinkedIn username of the receiver. |
| `message` | body | `string` | yes | Message to send to the receiver. |

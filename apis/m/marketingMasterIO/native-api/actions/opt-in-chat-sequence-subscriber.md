# Opt In Chat Sequence Subscriber with Marketing Master IO

Opts a subscriber into a chat sequence in Marketing Master IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messenger/chat_sequences/:chat_sequence_id/:subscriber_id`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Opt In Chat Sequence Subscriber](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chat_sequence_id` | path | `string` | yes |
| `subscriber_id` | path | `string` | yes |

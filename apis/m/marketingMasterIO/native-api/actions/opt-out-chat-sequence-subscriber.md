# Opt Out Chat Sequence Subscriber with Marketing Master IO

Removes a subscriber from a chat sequence in Marketing Master IO.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/messenger/chat_sequences/:chat_sequence_id/:subscriber_id`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Opt Out Chat Sequence Subscriber](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chat_sequence_id` | path | `string` | yes |
| `subscriber_id` | path | `string` | yes |

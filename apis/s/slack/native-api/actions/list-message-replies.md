# List Message Replies with Slack

Retrieves replies from a Slack conversation thread.

## Endpoint

- **Method:** `GET`
- **Path:** `conversations.replies`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [List Message Replies](https://docs.slack.dev/reference/methods/conversations.replies/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | query | `list<string>` | yes | Conversation ID to fetch thread from. |
| `ts` | query | `list<string>` | yes | Unique identifier of either a thread’s parent message or a message in the thread. ts must be the timestamp of an existing message with 0 or more replies. If there are no replies then just the single message referenced by ts will return - it is just an ordinary, unthreaded message. |
| `include_all_metadata` | query | `boolean<string>` | no | Return all metadata associated with this message. |
| `inclusive` | query | `boolean` | no | Include messages with oldest or latest timestamps in results. Ignored unless either timestamp is specified. |
| `latest` | query | `date` | no | Only messages before this Unix timestamp will be included in results. |
| `oldest` | query | `date` | no | Only messages after this Unix timestamp will be included in results. |

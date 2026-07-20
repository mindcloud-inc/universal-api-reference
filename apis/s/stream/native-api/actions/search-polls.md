# Search Polls with Stream

Finds polls in Stream by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/polls/query`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Search Polls](https://getstream.io/chat/docs/javascript/polls_api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | Poll query filter object. |
| `limit` | body | `number` | no | Maximum number of polls to return. |
| `user_id` | query | `string` | no | User ID query context. |

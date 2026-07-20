# Search Threads with Stream

Finds threads in Stream by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Search Threads](https://getstream.io/chat/docs/javascript/threads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | Thread query filter object. |
| `limit` | body | `number` | no | Maximum number of threads to return. |
| `user_id` | body | `string` | no | User ID context for the query. |

# BotHelp: List Subscribers

Retrieves subscriber records from BotHelp.

```
GET https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHelp `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/list-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/list-subscribers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Filter subscribers by email. |
| `phone` | string | no | Filter subscribers by phone. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | number | no | Subscriber pagination cursor by ID. |
| `createdAtAfter` | number | no | Return subscribers created after this Unix timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelName": "Ava Chen",
      "channelType": "string",
      "createdAt": 1,
      "cuid": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "subscribed": true,
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelName` | string | Channel name. |
| `channelType` | string | Channel type. |
| `createdAt` | number | Subscriber creation timestamp. |
| `cuid` | string | Subscriber CUID. |
| `email` | string | Subscriber email. |
| `id` | number | Subscriber ID. |
| `name` | string | Subscriber name. |
| `phone` | string | Subscriber phone. |
| `subscribed` | boolean | Whether the person is subscribed. |
| `tags` | array<string> | Subscriber tags. |

## Native endpoint

Through the native BotHelp API, this operation is `GET /v1/subscribers/` (base URL `https://api.bothelp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.


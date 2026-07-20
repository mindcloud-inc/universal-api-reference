# Social Intents: List Chats By Visitor

Retrieves chats from Social Intents by visitor ID.

```
GET https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-chats-by-visitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Social Intents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-chats-by-visitor?connectionId=$CONNECTION_ID&visitorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "visitorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-chats-by-visitor?${params}`, {
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
| `visitorId` | string | yes | Filter chats by visitor ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Social Intents API returns.

## Native endpoint

Through the native Social Intents API, this operation is `GET /chats` (base URL `https://www.socialintents.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chats-by-visitor.md) for the provider-specific parameters and requirements.


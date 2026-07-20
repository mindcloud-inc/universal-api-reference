# Social Intents: List Chats By Timezone

Retrieves chats from Social Intents by timezone.

```
GET https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-chats-by-timezone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Social Intents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-chats-by-timezone?connectionId=$CONNECTION_ID&timezone=America%2FNew_York" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timezone": "America/New_York"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-chats-by-timezone?${params}`, {
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
| `timezone` | string | yes | Filter chats by timezone. Example: `America/New_York`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Social Intents API returns.

## Native endpoint

Through the native Social Intents API, this operation is `GET /chats` (base URL `https://www.socialintents.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chats-by-timezone.md) for the provider-specific parameters and requirements.


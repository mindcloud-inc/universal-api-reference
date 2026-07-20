# Social Intents: List Widgets

Retrieves widgets from Social Intents.

```
GET https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-widgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Social Intents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-widgets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-widgets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "id": "string",
      "name": "Ava Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `id` | string |  |
| `name` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Social Intents API, this operation is `GET /apps` (base URL `https://www.socialintents.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-widgets.md) for the provider-specific parameters and requirements.


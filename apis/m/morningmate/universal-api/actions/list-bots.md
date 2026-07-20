# Morningmate: List Bots

Retrieves notification bots from Morningmate.

```
GET https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/list-bots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/list-bots?${params}`, {
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
      "botId": "string",
      "botName": "Ava Chen",
      "botProperty": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | string | Notification bot ID. |
| `botName` | string | Notification bot name. |
| `botProperty` | string | Notification bot property. |

## Native endpoint

Through the native Morningmate API, this operation is `GET /v1/bots` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bots.md) for the provider-specific parameters and requirements.


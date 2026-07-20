# Blue: List Webhooks

Retrieves configured webhooks from Blue.

```
GET https://connect.mindcloud.co/v1/universal/blue/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blue/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blue/latest/actions/list-webhooks?${params}`, {
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
      "enabled": true,
      "id": "string",
      "name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Blue API, this operation is `POST /graphql` (base URL `https://api.blue.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.


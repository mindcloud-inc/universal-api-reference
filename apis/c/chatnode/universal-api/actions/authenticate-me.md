# Chatnode: Authenticate Me



```
GET https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/authenticate-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatnode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/authenticate-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/authenticate-me?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Numeric team identifier returned by Chatnode. |
| `name` | string | Team name associated with the API key. |
| `slug` | string | Team slug associated with the API key; this tenant returns the provided GUID-style team identifier. |

## Native endpoint

Through the native Chatnode API, this operation is `GET auth_me` (base URL `https://api.public.chatnode.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate-me.md) for the provider-specific parameters and requirements.


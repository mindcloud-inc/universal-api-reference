# Supernotes: Get Users Tags

Retrieves your saved tags from Supernotes.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-users-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-users-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-users-tags?${params}`, {
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
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tag` | string |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /tags` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-users-tags.md) for the provider-specific parameters and requirements.


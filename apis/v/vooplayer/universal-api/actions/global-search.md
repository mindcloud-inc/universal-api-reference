# Vooplayer: Global Search

Finds matching records across your Vooplayer account.

```
GET https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/global-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vooplayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/global-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/global-search?${params}`, {
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
      "type": "string",
      "updated": "string",
      "videoGroup": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Matched resource ID. |
| `name` | string | Matched resource name. |
| `type` | string | Matched resource type. |
| `updated` | string | Last updated timestamp. |
| `videoGroup` | string | Owning project ID when applicable. |

## Native endpoint

Through the native Vooplayer API, this operation is `POST /search/global` (base URL `https://api.spotlightr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/global-search.md) for the provider-specific parameters and requirements.


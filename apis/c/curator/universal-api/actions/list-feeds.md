# Curator: List Feeds

Retrieves feeds from Curator.

```
GET https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Curator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-feeds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-feeds?${params}`, {
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
      "apiId": "string",
      "cacheTime": 1,
      "id": "string",
      "isLatestVersion": true,
      "moderation": "string",
      "name": "Ava Chen",
      "postCount": 1,
      "postStatus": 1,
      "publicKey": "string",
      "slug": "string",
      "type": "string",
      "widgetTheme": "string",
      "widgetType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiId` | string |  |
| `cacheTime` | number |  |
| `id` | string |  |
| `isLatestVersion` | boolean |  |
| `moderation` | string |  |
| `name` | string |  |
| `postCount` | number |  |
| `postStatus` | number |  |
| `publicKey` | string |  |
| `slug` | string |  |
| `type` | string |  |
| `widgetTheme` | string |  |
| `widgetType` | string |  |

## Native endpoint

Through the native Curator API, this operation is `GET /v1/feeds` (base URL `https://api.curator.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-feeds.md) for the provider-specific parameters and requirements.


# Curator: Update Feed

Updates an existing feed in Curator.

```
PUT https://connect.mindcloud.co/v1/universal/curator/latest/actions/update-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Curator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/curator/latest/actions/update-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/curator/latest/actions/update-feed', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedId` | string | yes | ID of the feed to update. |
| `name` | string | yes | Updated feed name. |

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

Through the native Curator API, this operation is `POST /v1/feeds/:FEED_ID` (base URL `https://api.curator.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-feed.md) for the provider-specific parameters and requirements.


# Curator: Create Feed

Creates a feed in Curator.

```
POST https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Curator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-feed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the feed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiId": "string",
      "cacheTime": 1,
      "defaultFeedLayoutId": 1,
      "id": "string",
      "isLatestVersion": true,
      "moderation": "string",
      "name": "Ava Chen",
      "publicKey": "string",
      "slug": "string",
      "widgetTheme": "string",
      "widgetType": "string",
      "widgetVersion": "string"
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
| `defaultFeedLayoutId` | number |  |
| `id` | string |  |
| `isLatestVersion` | boolean |  |
| `moderation` | string |  |
| `name` | string |  |
| `publicKey` | string |  |
| `slug` | string |  |
| `widgetTheme` | string |  |
| `widgetType` | string |  |
| `widgetVersion` | string |  |

## Native endpoint

Through the native Curator API, this operation is `POST /v1/feeds` (base URL `https://api.curator.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feed.md) for the provider-specific parameters and requirements.


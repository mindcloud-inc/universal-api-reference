# ImageKit.io: Purge Cache

Purges cached file URLs in ImageKit.io.

```
PUT https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/purge-cache
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/purge-cache" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/purge-cache', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | Default: `https://ik.imagekit.io/mindcloud/default-image.jpg?updatedAt=1771430880350`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string |  |

## Native endpoint

Through the native ImageKit.io API, this operation is `POST /files/purge` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purge-cache.md) for the provider-specific parameters and requirements.


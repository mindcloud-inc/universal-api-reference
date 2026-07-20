# Uniqode: Create Media Object

Creates a new media object in Uniqode.

```
POST https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/create-media-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/create-media-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/create-media-object', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "key": "string",
      "media_url": "https://example.com",
      "policy": "string",
      "post_action_url": "https://example.com",
      "x-amz-algorithm": "string",
      "x-amz-credential": "string",
      "x-amz-date": "string",
      "x-amz-signature": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `key` | string |  |
| `media_url` | string |  |
| `policy` | string |  |
| `post_action_url` | string |  |
| `x-amz-algorithm` | string |  |
| `x-amz-credential` | string |  |
| `x-amz-date` | string |  |
| `x-amz-signature` | string |  |

## Native endpoint

Through the native Uniqode API, this operation is `POST /media/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-media-object.md) for the provider-specific parameters and requirements.


# Sendbird: Create Open Channel



```
POST https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/create-open-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/create-open-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/create-open-channel', {
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
      "channelUrl": "https://example.com",
      "coverUrl": "https://example.com",
      "createdAt": 1,
      "freeze": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelUrl` | string |  |
| `coverUrl` | string |  |
| `createdAt` | number |  |
| `freeze` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Sendbird API, this operation is `POST /open_channels` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-open-channel.md) for the provider-specific parameters and requirements.


# Restream: Add Channel

Creates a streaming channel in Restream.

```
POST https://connect.mindcloud.co/v1/universal/restream/latest/actions/add-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/restream/latest/actions/add-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "platformId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restream/latest/actions/add-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "platformId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `platformId` | number | yes | Platform ID from Restream's platform list. |
| `streamKey` | string | no | Stream key, required for some platforms. |
| `streamUrl` | string | no | Stream URL, required for some platforms. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelUrl": "https://example.com",
      "displayName": "Ava Chen",
      "id": 1,
      "platformId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelUrl` | string |  |
| `displayName` | string |  |
| `id` | number |  |
| `platformId` | number |  |

## Native endpoint

Through the native Restream API, this operation is `POST /user/channels` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-channel.md) for the provider-specific parameters and requirements.


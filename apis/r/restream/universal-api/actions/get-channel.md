# Restream: Get Channel

Retrieves a streaming channel from Restream by ID.

```
GET https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-channel?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | number | yes | The ID of the channel to retrieve. |

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

Through the native Restream API, this operation is `GET /user/channels/:channelId` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.


# 2Chat: List Webhooks By Channel

Retrieves webhook subscriptions for a 2Chat channel.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-webhooks-by-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-webhooks-by-channel?connectionId=$CONNECTION_ID&channelUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-webhooks-by-channel?${params}`, {
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
| `channelUuid` | string | yes | The UUID of the channel to list webhook subscriptions for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /webhooks/channel/:channel_uuid` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks-by-channel.md) for the provider-specific parameters and requirements.


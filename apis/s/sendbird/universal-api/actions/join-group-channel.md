# Sendbird: Join Group Channel



```
PUT https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/join-group-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/join-group-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/join-group-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelUrl` | string | yes | The group channel URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelUrl": "https://example.com",
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
| `name` | string |  |

## Native endpoint

Through the native Sendbird API, this operation is `PUT /group_channels/:channelUrl/join` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/join-group-channel.md) for the provider-specific parameters and requirements.


# Sendbird: Delete Group Channel Metacounters



```
DELETE https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/delete-group-channel-metacounters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/delete-group-channel-metacounters?connectionId=$CONNECTION_ID&channelUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/delete-group-channel-metacounters?${params}`, {
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
| `channelUrl` | string | yes | The group channel URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelUrl` | string |  |

## Native endpoint

Through the native Sendbird API, this operation is `DELETE /group_channels/:channelUrl/metacounter` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-group-channel-metacounters.md) for the provider-specific parameters and requirements.


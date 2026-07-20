# Sendbird: List Group Channels



```
GET https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-group-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-group-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-group-channels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
      "customType": "string",
      "memberCount": 1,
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
| `customType` | string |  |
| `memberCount` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Sendbird API, this operation is `GET /group_channels` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-channels.md) for the provider-specific parameters and requirements.


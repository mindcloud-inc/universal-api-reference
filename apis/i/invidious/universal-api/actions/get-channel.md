# Invidious: Get Channel



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-channel?connectionId=$CONNECTION_ID&id=UC_x5XG1OV2P6uZZ5FSM9Ttw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "UC_x5XG1OV2P6uZZ5FSM9Ttw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-channel?${params}`, {
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
| `id` | string | yes | Channel UCID. Example: `UC_x5XG1OV2P6uZZ5FSM9Ttw`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "authorId": "string",
      "authorUrl": "https://example.com",
      "latestVideos": [
        {}
      ],
      "subCount": 1,
      "totalViews": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `authorId` | string |  |
| `authorUrl` | string |  |
| `latestVideos` | array<object> |  |
| `subCount` | number |  |
| `totalViews` | number |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /channels/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.


# Invidious: Search Channel



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/search-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/search-channel?connectionId=$CONNECTION_ID&channelId=UC_x5XG1OV2P6uZZ5FSM9Ttw&query=ambient%20music" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "UC_x5XG1OV2P6uZZ5FSM9Ttw",
  "query": "ambient music"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/search-channel?${params}`, {
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
| `channelId` | string | yes | Channel UCID. Example: `UC_x5XG1OV2P6uZZ5FSM9Ttw`. |
| `page` | number | no | Channel search page number. Example: `1`. |
| `query` | string | yes | Search text within the channel. Example: `ambient music`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "authorId": "string",
      "title": "string",
      "type": "string",
      "videoId": "string"
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
| `title` | string |  |
| `type` | string |  |
| `videoId` | string |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /channels/:ucid/search` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-channel.md) for the provider-specific parameters and requirements.


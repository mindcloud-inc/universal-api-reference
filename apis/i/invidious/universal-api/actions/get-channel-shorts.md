# Invidious: Get Channel Shorts



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-channel-shorts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-channel-shorts?connectionId=$CONNECTION_ID&id=UC_x5XG1OV2P6uZZ5FSM9Ttw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "UC_x5XG1OV2P6uZZ5FSM9Ttw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-channel-shorts?${params}`, {
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
| `continuation` | string | no | Continuation token. |
| `id` | string | yes | Channel UCID. Example: `UC_x5XG1OV2P6uZZ5FSM9Ttw`. |
| `sortBy` | string | no | Shorts sort order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "authorId": "string",
      "continuation": "string",
      "videos": [
        {}
      ]
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
| `continuation` | string |  |
| `videos` | array<object> |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /channels/:id/shorts` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-shorts.md) for the provider-specific parameters and requirements.


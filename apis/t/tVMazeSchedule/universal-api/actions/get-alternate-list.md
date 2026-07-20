# TVMaze Schedule: Get Alternate List

Retrieves an alternate list from TVMaze.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-alternate-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-alternate-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-alternate-list?${params}`, {
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
| `id` | number | yes | Required TVmaze alternate list ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `embed` | string | no | Optional embedded resource name, such as alternateepisodes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "broadcast_premiere": true,
      "country_premiere": true,
      "dvd_release": true,
      "id": 1,
      "language": {},
      "language_premiere": true,
      "network": {},
      "streaming_premiere": true,
      "url": "https://example.com",
      "verbatim_order": true,
      "webChannel": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `broadcast_premiere` | boolean |  |
| `country_premiere` | boolean |  |
| `dvd_release` | boolean |  |
| `id` | number |  |
| `language` | object |  |
| `language_premiere` | boolean |  |
| `network` | object |  |
| `streaming_premiere` | boolean |  |
| `url` | string |  |
| `verbatim_order` | boolean |  |
| `webChannel` | object |  |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /alternatelists/{{id}}` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alternate-list.md) for the provider-specific parameters and requirements.


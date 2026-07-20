# TVMaze Schedule: Get Alternate List With Alternate Episodes

Retrieves a TVMaze alternate list with episodes.

```
GET https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-alternate-list-with-alternate-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TVMaze Schedule `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-alternate-list-with-alternate-episodes?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-alternate-list-with-alternate-episodes?${params}`, {
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
| `id` | number | yes | TVMaze alternate list ID. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {},
      "_links": {},
      "country_premiere": "string",
      "dvd_release": "string",
      "id": 1,
      "name": "Ava Chen",
      "type": "string",
      "url": "https://example.com",
      "verbatim_order": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object |  |
| `_links` | object |  |
| `country_premiere` | string |  |
| `dvd_release` | string |  |
| `id` | number |  |
| `name` | string |  |
| `type` | string |  |
| `url` | string |  |
| `verbatim_order` | boolean |  |

## Native endpoint

Through the native TVMaze Schedule API, this operation is `GET /alternatelists/{{id}}` (base URL `https://api.tvmaze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alternate-list-with-alternate-episodes.md) for the provider-specific parameters and requirements.


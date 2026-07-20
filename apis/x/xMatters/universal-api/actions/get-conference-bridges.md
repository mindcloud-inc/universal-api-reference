# xMatters: Get conference bridges

Retrieves conference bridges from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-conference-bridges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-conference-bridges?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-conference-bridges?${params}`, {
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
      "count": 1,
      "data": [
        {
          "description": "string",
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "meetingLink": "https://example.com",
          "name": "Ava Chen",
          "pauseBeforeBridgePrompt": 1,
          "preferredConnectionType": "string",
          "staticBridgeNumber": true,
          "tollFreeNumber": "string",
          "tollNumber": "string"
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].meetingLink` | string |  |
| `data[].name` | string |  |
| `data[].pauseBeforeBridgePrompt` | number |  |
| `data[].preferredConnectionType` | string |  |
| `data[].staticBridgeNumber` | boolean |  |
| `data[].tollFreeNumber` | string |  |
| `data[].tollNumber` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET conference-bridges` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-conference-bridges.md) for the provider-specific parameters and requirements.


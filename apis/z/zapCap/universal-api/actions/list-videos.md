# ZapCap: List Videos

Retrieves videos from ZapCap.

```
GET https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/list-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/list-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/list-videos?${params}`, {
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
      "data": [
        {
          "filename": "Ava Chen",
          "id": "string",
          "metadata": {
            "duration": 1,
            "height": 1,
            "id": "string",
            "width": 1
          },
          "status": "string",
          "ttl": {},
          "videoTasks": [
            "string"
          ]
        }
      ],
      "limit": 1,
      "page": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].filename` | string |  |
| `data[].id` | string |  |
| `data[].metadata.duration` | number |  |
| `data[].metadata.height` | number |  |
| `data[].metadata.id` | string |  |
| `data[].metadata.width` | number |  |
| `data[].status` | string |  |
| `data[].ttl` | object |  |
| `data[].videoTasks[]` | string |  |
| `limit` | number |  |
| `page` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native ZapCap API, this operation is `GET /videos` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-videos.md) for the provider-specific parameters and requirements.


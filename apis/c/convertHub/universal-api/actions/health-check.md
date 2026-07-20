# ConvertHub: Health Check

Retrieves API health and statistics from ConvertHub.

```
GET https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/health-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/health-check?${params}`, {
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
      "api_version": "string",
      "stats": {
        "total_conversions": 1,
        "total_formats": 1
      },
      "status": "string",
      "success": true,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_version` | string |  |
| `stats` | object |  |
| `stats.total_conversions` | number |  |
| `stats.total_formats` | number |  |
| `status` | string |  |
| `success` | boolean |  |
| `timestamp` | string |  |

## Native endpoint

Through the native ConvertHub API, this operation is `GET /v2/health` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health-check.md) for the provider-specific parameters and requirements.


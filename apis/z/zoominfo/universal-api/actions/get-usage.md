# Zoominfo: Get Usage

Retrieves usage details from ZoomInfo.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-usage?${params}`, {
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
      "usage": [
        {
          "currentUsage": 1,
          "description": "string",
          "limitType": "string",
          "totalLimit": 1,
          "usageRemaining": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `usage[].currentUsage` | number |  |
| `usage[].description` | string |  |
| `usage[].limitType` | string |  |
| `usage[].totalLimit` | number |  |
| `usage[].usageRemaining` | number |  |

## Native endpoint

Through the native Zoominfo API, this operation is `GET lookup/usage` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.


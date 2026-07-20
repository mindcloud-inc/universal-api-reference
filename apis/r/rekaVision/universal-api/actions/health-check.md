# Reka Vision: Health Check

Retrieves the Reka Vision service health status.

```
GET https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/health-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/health-check?${params}`, {
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
      "healthy": true,
      "mode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `healthy` | boolean |  |
| `mode` | string |  |

## Native endpoint

Through the native Reka Vision API, this operation is `GET /health` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health-check.md) for the provider-specific parameters and requirements.


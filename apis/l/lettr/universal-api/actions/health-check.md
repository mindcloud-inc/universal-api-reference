# Lettr: Health Check



```
GET https://connect.mindcloud.co/v1/universal/lettr/latest/actions/health-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/health-check?${params}`, {
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
      "data": {
        "status": "string",
        "timestamp": "2026-05-07T12:00:00.000Z"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Health payload. |
| `data.status` | string | Current API status. |
| `data.timestamp` | date | ISO 8601 health timestamp. |
| `message` | string | Health status message. |

## Native endpoint

Through the native Lettr API, this operation is `GET /health` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health-check.md) for the provider-specific parameters and requirements.


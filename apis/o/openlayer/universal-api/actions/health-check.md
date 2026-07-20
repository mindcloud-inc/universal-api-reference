# Openlayer: Health Check

Retrieves health check status from Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/health-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/health-check?${params}`, {
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
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Health-check response text. |

## Native endpoint

Through the native Openlayer API, this operation is `GET /diagnostics/health-check` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health-check.md) for the provider-specific parameters and requirements.


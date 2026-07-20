# Vistaly: Health Check

Retrieves health status from Vistaly.

```
GET https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/health-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vistaly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/health-check?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Vistaly API, this operation is `GET /v1/health` (base URL `https://api.vistaly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health-check.md) for the provider-specific parameters and requirements.


# SMMCode: List Services



```
GET https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMMCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/list-services?${params}`, {
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
      "category": "string",
      "max": "string",
      "min": "string",
      "name": "Ava Chen",
      "rate": "string",
      "service": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Service category. |
| `max` | string | Maximum quantity. |
| `min` | string | Minimum quantity. |
| `name` | string | Service name. |
| `rate` | string | Service rate. |
| `service` | number | Service ID. |
| `type` | string | Service type. |

## Native endpoint

Through the native SMMCode API, this operation is `POST /api/v2` (base URL `https://extended.smmcode.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.


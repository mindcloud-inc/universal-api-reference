# Calculoid: Get Geo IP



```
GET https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/get-geo-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/get-geo-ip?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/get-geo-ip?${params}`, {
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
      "code_2": "string",
      "code_3": "string",
      "id": "string",
      "is_eu": "string",
      "name": "Ava Chen",
      "phone_prefix": "string",
      "vat_percent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code_2` | string |  |
| `code_3` | string |  |
| `id` | string |  |
| `is_eu` | string |  |
| `name` | string |  |
| `phone_prefix` | string |  |
| `vat_percent` | string |  |

## Native endpoint

Through the native Calculoid API, this operation is `GET /geoIP/` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-geo-ip.md) for the provider-specific parameters and requirements.


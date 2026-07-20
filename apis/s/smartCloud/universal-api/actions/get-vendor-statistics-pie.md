# 2Smart Cloud: Pie statistics



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-statistics-pie
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-statistics-pie?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-statistics-pie?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product_id` | number | no | ID of product |

## Response

```json
{
  "success": true,
  "data": [
    {
      "offline": 1,
      "online": 1,
      "product_id": 1,
      "product_title": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `offline` | number |  |
| `online` | number |  |
| `product_id` | number |  |
| `product_title` | string |  |
| `total` | number |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /vendor/statistics/pie` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor-statistics-pie.md) for the provider-specific parameters and requirements.


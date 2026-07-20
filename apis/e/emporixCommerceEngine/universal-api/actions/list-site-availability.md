# Emporix Commerce Engine: List Site Availability

Retrieves site availability from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-site-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-site-availability?connectionId=$CONNECTION_ID&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-site-availability?${params}`, {
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
| `site` | string | yes | The Emporix site code to retrieve availability for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true,
      "distributionChannel": "string",
      "id": "string",
      "metadata": {},
      "popularity": 1,
      "productId": "string",
      "site": "string",
      "stockLevel": 1,
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean |  |
| `distributionChannel` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `popularity` | number |  |
| `productId` | string |  |
| `site` | string |  |
| `stockLevel` | number |  |
| `vendorId` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /availability/{{credentials.tenantId}}/availability/site/:site` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-site-availability.md) for the provider-specific parameters and requirements.


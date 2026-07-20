# 2Smart Cloud: Approve products



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-products-approve
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-products-approve?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-products-approve?${params}`, {
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
| `id[]` | array<number> | no | IDs of entities |
| `type` | string | no | Type of product |
| `abbreviation` | number | no | Abbreviation of product |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "id": 1,
      "is_approved": true,
      "is_show_market": true,
      "is_show_schema": true,
      "title": "string",
      "updated": "string",
      "vendor_email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `id` | number |  |
| `is_approved` | boolean |  |
| `is_show_market` | boolean |  |
| `is_show_schema` | boolean |  |
| `title` | string |  |
| `updated` | string |  |
| `vendor_email` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /vendor/products/approve` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor-products-approve.md) for the provider-specific parameters and requirements.


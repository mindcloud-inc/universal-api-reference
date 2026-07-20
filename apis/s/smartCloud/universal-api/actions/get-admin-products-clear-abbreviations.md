# 2Smart Cloud: Clear products abbreviations



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-admin-products-clear-abbreviations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-admin-products-clear-abbreviations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-admin-products-clear-abbreviations?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_approved": true,
      "is_show_market": true,
      "is_show_schema": true,
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "vendor_email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | number |  |
| `is_approved` | boolean |  |
| `is_show_market` | boolean |  |
| `is_show_schema` | boolean |  |
| `title` | string |  |
| `updated` | date |  |
| `vendor_email` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /admin/products/clear-abbreviations` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-admin-products-clear-abbreviations.md) for the provider-specific parameters and requirements.


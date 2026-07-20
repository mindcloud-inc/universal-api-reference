# Cloudprinter.com: Get Product Info

Retrieves product details from Cloudprinter.com.

```
GET https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/get-product-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudprinter.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/get-product-info?connectionId=$CONNECTION_ID&reference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/get-product-info?${params}`, {
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
| `reference` | string | yes | Product reference returned by List Products. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": "string",
      "files": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "note": "string",
      "options": [
        [
          {}
        ]
      ],
      "reference": "string",
      "specs": [
        [
          {}
        ]
      ],
      "sub_category_type_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | string |  |
| `files[]` | array<object> |  |
| `files[].format` | string |  |
| `files[].template` | string |  |
| `files[].type` | string |  |
| `name` | string |  |
| `note` | string |  |
| `options[]` | array<object> |  |
| `options[].availability` | string |  |
| `options[].default` | number |  |
| `options[].files[]` | array<object> |  |
| `options[].files[].format` | string |  |
| `options[].files[].type` | string |  |
| `options[].note` | string |  |
| `options[].reference` | string |  |
| `options[].type` | string |  |
| `options[].type_name` | string |  |
| `reference` | string |  |
| `specs[]` | array<object> |  |
| `specs[].note` | string |  |
| `specs[].reference` | string |  |
| `specs[].value` | string |  |
| `sub_category_type_id` | number |  |

## Native endpoint

Through the native Cloudprinter.com API, this operation is `POST /cloudcore/1.0/products/info` (base URL `https://api.cloudprinter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-info.md) for the provider-specific parameters and requirements.


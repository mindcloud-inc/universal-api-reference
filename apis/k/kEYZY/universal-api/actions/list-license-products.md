# KEYZY: List License Products

Retrieves products related to a KEYZY license.

```
GET https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/list-license-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/list-license-products?connectionId=$CONNECTION_ID&serial=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serial": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/list-license-products?${params}`, {
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
| `serial` | string | yes | Serial number of the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "active": true,
          "code": "string",
          "createdAt": "string",
          "filename": "Ava Chen",
          "id": 1,
          "key": "string",
          "maxHostCount": 1,
          "name": "Ava Chen",
          "signature": "string",
          "signatureTrial": "string",
          "updatedAt": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].active` | boolean | Whether the product is active. |
| `data[].code` | string | Product code. |
| `data[].createdAt` | string | Creation timestamp. |
| `data[].filename` | string | Filename. |
| `data[].id` | number | Product ID. |
| `data[].key` | string | Product key. |
| `data[].maxHostCount` | number | Maximum host count. |
| `data[].name` | string | Product name. |
| `data[].signature` | string | Signature value. |
| `data[].signatureTrial` | string | Trial signature value. |
| `data[].updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native KEYZY API, this operation is `POST /licenses/products` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-license-products.md) for the provider-specific parameters and requirements.


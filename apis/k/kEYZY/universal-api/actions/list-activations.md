# KEYZY: List Activations

Retrieves activations for a KEYZY license serial number.

```
GET https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/list-activations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/list-activations?connectionId=$CONNECTION_ID&serial=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serial": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/list-activations?${params}`, {
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
| `serial` | string | yes | A license serial number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "activated": true,
          "createdAt": "string",
          "deviceTag": "string",
          "hostId": "string",
          "id": 1,
          "licenseId": 1,
          "productId": 1,
          "productName": "Ava Chen",
          "serial": "string",
          "sku": "string",
          "skuName": "Ava Chen",
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
| `data[].activated` | boolean | Whether the activation is active. |
| `data[].createdAt` | string | Creation timestamp. |
| `data[].deviceTag` | string | Device tag. |
| `data[].hostId` | string | Host identifier. |
| `data[].id` | number | Activation ID. |
| `data[].licenseId` | number | License ID. |
| `data[].productId` | number | Product ID. |
| `data[].productName` | string | Product name. |
| `data[].serial` | string | License serial number. |
| `data[].sku` | string | SKU number. |
| `data[].skuName` | string | SKU name. |
| `data[].updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native KEYZY API, this operation is `GET /activations/:serial` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activations.md) for the provider-specific parameters and requirements.


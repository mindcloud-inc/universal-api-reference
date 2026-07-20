# Cryptolens: Get Customer Licenses

Retrieves license keys for a customer from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-customer-licenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-customer-licenses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-customer-licenses?${params}`, {
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
      "block": true,
      "created": "string",
      "expires": "string",
      "f1": true,
      "f2": true,
      "f3": true,
      "f4": true,
      "f5": true,
      "f6": true,
      "f7": true,
      "f8": true,
      "globalId": 1,
      "id": 1,
      "key": "string",
      "notes": "string",
      "period": 1,
      "productId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block` | boolean | Get Customer Licenses response field `block` from Cryptolens docs example. |
| `created` | string | Get Customer Licenses response field `created` from Cryptolens docs example. |
| `expires` | string | Get Customer Licenses response field `expires` from Cryptolens docs example. |
| `f1` | boolean | Get Customer Licenses response field `f1` from Cryptolens docs example. |
| `f2` | boolean | Get Customer Licenses response field `f2` from Cryptolens docs example. |
| `f3` | boolean | Get Customer Licenses response field `f3` from Cryptolens docs example. |
| `f4` | boolean | Get Customer Licenses response field `f4` from Cryptolens docs example. |
| `f5` | boolean | Get Customer Licenses response field `f5` from Cryptolens docs example. |
| `f6` | boolean | Get Customer Licenses response field `f6` from Cryptolens docs example. |
| `f7` | boolean | Get Customer Licenses response field `f7` from Cryptolens docs example. |
| `f8` | boolean | Get Customer Licenses response field `f8` from Cryptolens docs example. |
| `globalId` | number | Get Customer Licenses response field `globalId` from Cryptolens docs example. |
| `id` | number | Get Customer Licenses response field `id` from Cryptolens docs example. |
| `key` | string | Get Customer Licenses response field `key` from Cryptolens docs example. |
| `notes` | string | Get Customer Licenses response field `notes` from Cryptolens docs example. |
| `period` | number | Get Customer Licenses response field `period` from Cryptolens docs example. |
| `productId` | number | Get Customer Licenses response field `productId` from Cryptolens docs example. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/customer/GetCustomerLicenses` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-licenses.md) for the provider-specific parameters and requirements.


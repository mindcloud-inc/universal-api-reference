# Cryptolens: Get Keys

Retrieves license keys for a product from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-keys?connectionId=$CONNECTION_ID&productId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-keys?${params}`, {
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
| `productId` | number | yes | The product id. |
| `page` | number | no | If there are more than 100 keys, only 99 will be returned on the first page. Increment this parameter by 1 to obtain the remaining licenses. Default: `1`. |
| `orderBy` | string | no | Specifies the way to order the result. |
| `searchQuery` | string | no | Restricts the result to only the license keys that satisfy the criterion. |
| `globalId` | number | no | If you need to find a specific license key, set this parameter to its ID for a faster response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "licenseKey": [
        {}
      ],
      "pageCount": 1,
      "returned": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `licenseKey` | array<object> | Get Keys response field `licenseKey` from Cryptolens docs example. |
| `pageCount` | number | Get Keys response field `pageCount` from Cryptolens docs example. |
| `returned` | number | Get Keys response field `returned` from Cryptolens docs example. |
| `total` | number | Get Keys response field `total` from Cryptolens docs example. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/product/GetKeys` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-keys.md) for the provider-specific parameters and requirements.


# Kladana: Get Product Directory Settings

Retrieves product directory settings from Kladana.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-product-directory-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-product-directory-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-product-directory-settings?${params}`, {
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
      "barcodeRules": {},
      "created": "2026-05-07T12:00:00.000Z",
      "meta": {},
      "productCodeGenerationType": "string",
      "uniqueCodeRules": {},
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcodeRules` | object | Product directory barcode rules. |
| `created` | date | Creation timestamp. |
| `meta` | object | Kladana metadata reference. |
| `productCodeGenerationType` | string | Product code generation mode. |
| `uniqueCodeRules` | object | Product directory unique-code rules. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/assortment/settings` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-directory-settings.md) for the provider-specific parameters and requirements.


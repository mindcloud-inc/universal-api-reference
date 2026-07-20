# Kladana: Get Company Settings

Retrieves company settings details from Kladana.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-company-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-company-settings?${params}`, {
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
      "checkShippingStock": true,
      "country": {},
      "currency": {},
      "discountStrategy": "string",
      "meta": {},
      "priceTypes": [
        {}
      ],
      "shared": true,
      "updated": "2026-05-07T12:00:00.000Z",
      "vatEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkShippingStock` | boolean | Whether stock is checked on shipment. |
| `country` | object | Company country. |
| `currency` | object | Default company currency. |
| `discountStrategy` | string | Discount strategy. |
| `meta` | object | Kladana metadata reference. |
| `priceTypes` | array<object> | Configured price types. |
| `shared` | boolean | Whether shared access is enabled. |
| `updated` | date | Last update timestamp. |
| `vatEnabled` | boolean | Whether VAT accounting is enabled. |

## Native endpoint

Through the native Kladana API, this operation is `GET /context/companysettings` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-settings.md) for the provider-specific parameters and requirements.


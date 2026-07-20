# Bookvault: List Promo Codes

Retrieves promotional codes from Bookvault.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-promo-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-promo-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-promo-codes?${params}`, {
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
      "Category": "string",
      "PromoCode": "string",
      "PromoEnd": "string",
      "PromoID": 1,
      "PromoStart": "string",
      "PromoType": "string",
      "PromoValue": 1,
      "UsageLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Category` | string |  |
| `PromoCode` | string |  |
| `PromoEnd` | string |  |
| `PromoID` | number |  |
| `PromoStart` | string |  |
| `PromoType` | string |  |
| `PromoValue` | number |  |
| `UsageLimit` | number |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Promos` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-promo-codes.md) for the provider-specific parameters and requirements.


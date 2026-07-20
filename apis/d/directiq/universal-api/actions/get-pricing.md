# DirectIQ: Get pricing

Retrieves current pricing details from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-pricing?${params}`, {
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
      "description": "string",
      "name": "Ava Chen",
      "subscriptionPlanPrices": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `name` | string |  |
| `subscriptionPlanPrices[]` | array<object> |  |
| `subscriptionPlanPrices[].numberOfContacts` | number |  |
| `subscriptionPlanPrices[].price` | number |  |
| `subscriptionPlanPrices[].priceAnnual` | number |  |
| `subscriptionPlanPrices[].priceAnnualTry` | number |  |
| `subscriptionPlanPrices[].priceTry` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /core/pricing` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pricing.md) for the provider-specific parameters and requirements.


# Namsor: Api Usage

Retrieves current Namsor API usage details.

```
GET https://connect.mindcloud.co/v1/universal/namsor/latest/actions/api-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Namsor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/api-usage?${params}`, {
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
      "billingPeriod": {},
      "overageCurrency": "string",
      "overageExclTax": 1,
      "overageInclTax": 1,
      "overageInclTaxAfterDiscount": 1,
      "overageQuantity": 1,
      "subscription": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingPeriod` | object |  |
| `overageCurrency` | string |  |
| `overageExclTax` | number |  |
| `overageInclTax` | number |  |
| `overageInclTaxAfterDiscount` | number |  |
| `overageQuantity` | number |  |
| `subscription` | object |  |

## Native endpoint

Through the native Namsor API, this operation is `GET /api2/json/apiUsage` (base URL `https://v2.namsor.com/NamSorAPIv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/api-usage.md) for the provider-specific parameters and requirements.


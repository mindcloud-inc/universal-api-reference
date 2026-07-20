# Convert: List Billing Plans

Retrieves available billing plans from Convert.

```
GET https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-billing-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-billing-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-billing-plans?${params}`, {
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
      "availableFeaturesIds": [
        1
      ],
      "availableFeaturesNiceNames": [
        "Ava Chen"
      ],
      "billingCycleDuration": "string",
      "contract": "string",
      "id": 1,
      "name": "Ava Chen",
      "price": 1,
      "product": "string",
      "usage_limit_by": "string",
      "usageLimits": {
        "domains": {
          "limitValue": "string"
        },
        "goals": {
          "limitValue": 1
        },
        "projects": {
          "limitValue": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableFeaturesIds[]` | number |  |
| `availableFeaturesNiceNames[]` | string |  |
| `billingCycleDuration` | string |  |
| `contract` | string |  |
| `id` | number |  |
| `name` | string |  |
| `price` | number |  |
| `product` | string |  |
| `usage_limit_by` | string |  |
| `usageLimits.domains.limitValue` | string |  |
| `usageLimits.goals.limitValue` | number |  |
| `usageLimits.projects.limitValue` | number |  |

## Native endpoint

Through the native Convert API, this operation is `GET /billing-plans` (base URL `https://api.convert.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing-plans.md) for the provider-specific parameters and requirements.


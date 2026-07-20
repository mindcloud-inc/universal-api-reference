# Convert: List Accounts

Retrieves the available accounts from Convert.

```
GET https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-accounts-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-accounts-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-accounts-list?${params}`, {
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
      "access_all_projects": true,
      "accessRole": "string",
      "accountType": "string",
      "all": true,
      "billing": {
        "details": {
          "billingType": "string",
          "currentBillingCycleStart": 1,
          "isPausedByQuota": true,
          "nextBillingCycleStart": 1
        },
        "products": {
          "experiences": {
            "plan": {
              "id": 1,
              "name": "Ava Chen"
            }
          }
        }
      },
      "id": 1,
      "limitsAndCapabilities": {
        "usage_limit_by": "string"
      },
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_all_projects` | boolean |  |
| `accessRole` | string |  |
| `accountType` | string |  |
| `all` | boolean |  |
| `billing.details.billingType` | string |  |
| `billing.details.currentBillingCycleStart` | number |  |
| `billing.details.isPausedByQuota` | boolean |  |
| `billing.details.nextBillingCycleStart` | number |  |
| `billing.products.experiences.plan.id` | number |  |
| `billing.products.experiences.plan.name` | string |  |
| `id` | number |  |
| `limitsAndCapabilities.usage_limit_by` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Convert API, this operation is `GET /accounts` (base URL `https://api.convert.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-accounts-list.md) for the provider-specific parameters and requirements.


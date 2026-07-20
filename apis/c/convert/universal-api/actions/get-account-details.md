# Convert: Get Account Details

Retrieves detailed account information from Convert.

```
GET https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-account-details?${params}`, {
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
          "company": "string",
          "isPausedByQuota": true,
          "pending_cancellation": true
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
      "name": "Ava Chen",
      "settings": {
        "single_sign_on_status": "string"
      }
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
| `billing.details.company` | string |  |
| `billing.details.isPausedByQuota` | boolean |  |
| `billing.details.pending_cancellation` | boolean |  |
| `billing.products.experiences.plan.id` | number |  |
| `billing.products.experiences.plan.name` | string |  |
| `id` | number |  |
| `limitsAndCapabilities.usage_limit_by` | string |  |
| `name` | string |  |
| `settings.single_sign_on_status` | string |  |

## Native endpoint

Through the native Convert API, this operation is `GET /accounts/:account_id/details` (base URL `https://api.convert.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.


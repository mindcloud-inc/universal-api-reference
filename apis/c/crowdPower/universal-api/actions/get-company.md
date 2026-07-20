# CrowdPower: Get Company

Retrieves a company from CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-company?${params}`, {
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
| `companyId` | string | yes | Company identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "customers_count": 1,
      "customers_limit": 1,
      "id": "string",
      "is_paused": true,
      "is_subscribed": true,
      "is_suspended": true,
      "is_trialing": true,
      "monthly_email_count": 1,
      "monthly_email_limit": 1,
      "name": "Ava Chen",
      "onboarded": true,
      "slug": "string",
      "steps": {},
      "stripe_id": "string",
      "trial_ended_at": 1,
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `customers_count` | number |  |
| `customers_limit` | number |  |
| `id` | string |  |
| `is_paused` | boolean |  |
| `is_subscribed` | boolean |  |
| `is_suspended` | boolean |  |
| `is_trialing` | boolean |  |
| `monthly_email_count` | number |  |
| `monthly_email_limit` | number |  |
| `name` | string |  |
| `onboarded` | boolean |  |
| `slug` | string |  |
| `steps` | object |  |
| `stripe_id` | string |  |
| `trial_ended_at` | number |  |
| `updated_at` | number |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET companies/:company_id` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.


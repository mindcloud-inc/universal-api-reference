# CrowdPower: Get Projects

Retrieves projects for a company in CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-projects?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-projects?${params}`, {
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
      "charges_count": 1,
      "charges_sum": 1,
      "company_id": "string",
      "created_at": 1,
      "currency": "string",
      "customers_count": 1,
      "id": "string",
      "name": "Ava Chen",
      "onboarded": true,
      "slug": "string",
      "smtp_config": {},
      "theme": {},
      "updated_at": 1,
      "user_id": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charges_count` | number |  |
| `charges_sum` | number |  |
| `company_id` | string |  |
| `created_at` | number |  |
| `currency` | string |  |
| `customers_count` | number |  |
| `id` | string |  |
| `name` | string |  |
| `onboarded` | boolean |  |
| `slug` | string |  |
| `smtp_config` | object |  |
| `theme` | object |  |
| `updated_at` | number |  |
| `user_id` | string |  |
| `website` | string |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET companies/:company_id/projects` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-projects.md) for the provider-specific parameters and requirements.


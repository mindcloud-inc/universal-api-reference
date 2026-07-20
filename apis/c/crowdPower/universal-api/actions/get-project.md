# CrowdPower: Get Project

Retrieves a project from CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-project?${params}`, {
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
      "charges_count": 1,
      "charges_sum": 1,
      "company": {},
      "company_id": "string",
      "created_at": 1,
      "currency": "string",
      "customers_count": 1,
      "events": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "onboarded": true,
      "segments": [
        {}
      ],
      "slug": "string",
      "smtp_config": {},
      "tags": [
        {}
      ],
      "theme": {},
      "traits": [
        {}
      ],
      "unsub_groups": [
        {}
      ],
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
| `company` | object |  |
| `company_id` | string |  |
| `created_at` | number |  |
| `currency` | string |  |
| `customers_count` | number |  |
| `events` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `onboarded` | boolean |  |
| `segments` | array<object> |  |
| `slug` | string |  |
| `smtp_config` | object |  |
| `tags` | array<object> |  |
| `theme` | object |  |
| `traits` | array<object> |  |
| `unsub_groups` | array<object> |  |
| `updated_at` | number |  |
| `user_id` | string |  |
| `website` | string |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET projects/{{credentials.projectId}}` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.


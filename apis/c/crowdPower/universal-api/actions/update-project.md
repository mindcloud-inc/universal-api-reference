# CrowdPower: Update Project

Updates an existing project in CrowdPower.

```
PUT https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Project name. |
| `website` | string | no | Project website URL. |

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

Through the native CrowdPower API, this operation is `PUT projects/{{credentials.projectId}}` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.


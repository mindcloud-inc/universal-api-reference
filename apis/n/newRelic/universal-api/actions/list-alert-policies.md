# New Relic: List Alert Policies

Retrieves alert policies from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-alert-policies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-alert-policies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-alert-policies?${params}`, {
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
      "policies": [
        {
          "created_at": 1,
          "id": 1,
          "incident_preference": "string",
          "name": "Ava Chen",
          "updated_at": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `policies[].created_at` | number |  |
| `policies[].id` | number |  |
| `policies[].incident_preference` | string |  |
| `policies[].name` | string |  |
| `policies[].updated_at` | number |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /alerts_policies.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alert-policies.md) for the provider-specific parameters and requirements.


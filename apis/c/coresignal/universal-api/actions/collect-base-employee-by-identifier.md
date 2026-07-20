# Coresignal: Collect Base Employee By Identifier

Collects a base employee from Coresignal by identifier.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-employee-by-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-employee-by-identifier?connectionId=$CONNECTION_ID&employeeIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-employee-by-identifier?${params}`, {
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
| `employeeIdentifier` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_experience_title": "string",
      "connections_count": 1,
      "country": "string",
      "follower_count": 1,
      "full_name": "Ava Chen",
      "headline": "string",
      "id": 1,
      "location": "string",
      "profile_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_experience_title` | string |  |
| `connections_count` | number |  |
| `country` | string |  |
| `follower_count` | number |  |
| `full_name` | string |  |
| `headline` | string |  |
| `id` | number |  |
| `location` | string |  |
| `profile_url` | string |  |

## Native endpoint

Through the native Coresignal API, this operation is `GET /employee_base/collect/:employeeIdentifier` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/collect-base-employee-by-identifier.md) for the provider-specific parameters and requirements.


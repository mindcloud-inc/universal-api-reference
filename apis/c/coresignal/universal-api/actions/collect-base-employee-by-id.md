# Coresignal: Collect Base Employee By ID

Collects a base employee from Coresignal by ID.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-employee-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-employee-by-id?connectionId=$CONNECTION_ID&employeeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-employee-by-id?${params}`, {
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
| `employeeId` | number | yes |  |

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

Through the native Coresignal API, this operation is `GET /employee_base/collect/:employeeId` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/collect-base-employee-by-id.md) for the provider-specific parameters and requirements.


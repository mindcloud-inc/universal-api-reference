# Coresignal: Collect Multi-source Employee By Identifier

Collects a multi-source employee from Coresignal by identifier.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-employee-by-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-employee-by-identifier?connectionId=$CONNECTION_ID&employeeIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-employee-by-identifier?${params}`, {
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
      "followers_count": 1,
      "full_name": "Ava Chen",
      "headline": "string",
      "id": 1,
      "linkedin_url": "https://example.com",
      "location_city": "string",
      "location_country": "string"
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
| `followers_count` | number |  |
| `full_name` | string |  |
| `headline` | string |  |
| `id` | number |  |
| `linkedin_url` | string |  |
| `location_city` | string |  |
| `location_country` | string |  |

## Native endpoint

Through the native Coresignal API, this operation is `GET /employee_multi_source/collect/:employeeIdentifier` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/collect-multi-source-employee-by-identifier.md) for the provider-specific parameters and requirements.


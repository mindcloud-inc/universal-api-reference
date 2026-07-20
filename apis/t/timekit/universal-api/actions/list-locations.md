# Timekit: List Locations

Lists all available locations in Timekit.

```
GET https://connect.mindcloud.co/v1/universal/timekit/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timekit/latest/actions/list-locations?${params}`, {
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
| `include` | string | no |  |
| `search` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "distance": 1,
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "meta": {
        "t_latitude": "string",
        "t_longitude": "string",
        "t_store_address": "string",
        "t_store_capacity": "string",
        "t_store_city": "string",
        "t_store_code": "string",
        "t_store_country": "string",
        "t_store_country_name": "Ava Chen",
        "t_store_disabled": "string",
        "t_store_id": "string",
        "t_store_name": "Ava Chen",
        "t_store_phone": "string",
        "t_store_postal_code": "string",
        "t_store_region": "string",
        "t_store_region_name": "Ava Chen",
        "t_store_timezone": "string"
      },
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "use_custom_hours": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `distance` | number |  |
| `id` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `meta.t_latitude` | string |  |
| `meta.t_longitude` | string |  |
| `meta.t_store_address` | string |  |
| `meta.t_store_capacity` | string |  |
| `meta.t_store_city` | string |  |
| `meta.t_store_code` | string |  |
| `meta.t_store_country` | string |  |
| `meta.t_store_country_name` | string |  |
| `meta.t_store_disabled` | string |  |
| `meta.t_store_id` | string |  |
| `meta.t_store_name` | string |  |
| `meta.t_store_phone` | string |  |
| `meta.t_store_postal_code` | string |  |
| `meta.t_store_region` | string |  |
| `meta.t_store_region_name` | string |  |
| `meta.t_store_timezone` | string |  |
| `name` | string |  |
| `updated_at` | date |  |
| `use_custom_hours` | boolean |  |

## Native endpoint

Through the native Timekit API, this operation is `GET /locations` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.


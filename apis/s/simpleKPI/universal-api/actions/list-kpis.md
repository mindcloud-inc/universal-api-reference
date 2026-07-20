# SimpleKPI: List KPIs

Retrieves KPI records from a SimpleKPI account.

```
GET https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-kpis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-kpis?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-kpis?${params}`, {
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
      "aggregate_function": "string",
      "category_id": 1,
      "created_at": "string",
      "description": "string",
      "frequency_id": "string",
      "icon_id": 1,
      "id": 1,
      "is_active": true,
      "is_calculated": true,
      "name": "Ava Chen",
      "sort_order": 1,
      "target_default": "string",
      "unit_id": 1,
      "updated_at": "string",
      "value_direction": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregate_function` | string |  |
| `category_id` | number |  |
| `created_at` | string |  |
| `description` | string |  |
| `frequency_id` | string |  |
| `icon_id` | number |  |
| `id` | number |  |
| `is_active` | boolean |  |
| `is_calculated` | boolean |  |
| `name` | string |  |
| `sort_order` | number |  |
| `target_default` | string |  |
| `unit_id` | number |  |
| `updated_at` | string |  |
| `value_direction` | string |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `GET kpis` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-kpis.md) for the provider-specific parameters and requirements.


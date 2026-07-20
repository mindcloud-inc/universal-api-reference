# SimpleKPI: Create KPI

Creates a new KPI in SimpleKPI.

```
POST https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-kpi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-kpi" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-kpi', {
  method: 'POST',
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
| `aggregate_function` | string | no | The KPI aggregate function: AVG or SUM. |
| `category_id` | number | no | The SimpleKPI category ID to assign to the KPI. |
| `description` | string | no | The KPI description. |
| `frequency_id` | string | no | The SimpleKPI frequency ID to assign to the KPI. |
| `icon_id` | number | no | The SimpleKPI icon ID to assign to the KPI. |
| `is_active` | boolean | no | Whether the KPI is active. |
| `name` | string | no | The KPI name. |
| `sort_order` | number | no | The display sort order for the KPI. |
| `target_default` | number | no | The default KPI target value. |
| `unit_id` | number | no | The SimpleKPI unit ID to assign to the KPI. |
| `value_direction` | string | no | The KPI value direction: U, D, or N. |

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
      "is_calculated": "string",
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
| `is_calculated` | string |  |
| `name` | string |  |
| `sort_order` | number |  |
| `target_default` | string |  |
| `unit_id` | number |  |
| `updated_at` | string |  |
| `value_direction` | string |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `POST kpis` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-kpi.md) for the provider-specific parameters and requirements.


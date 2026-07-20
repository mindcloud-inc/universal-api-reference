# SimpleKPI: Get KPI Unit

Retrieves a KPI unit from SimpleKPI.

```
GET https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-kpi-unit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-kpi-unit?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-kpi-unit?${params}`, {
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
| `id` | number | yes | SimpleKPI KPI unit ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "display_format": "string",
      "entry_format": "string",
      "id": 1,
      "is_percentage": true,
      "name": "Ava Chen",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `display_format` | string |  |
| `entry_format` | string |  |
| `id` | number |  |
| `is_percentage` | boolean |  |
| `name` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `GET kpiunits/:id` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-kpi-unit.md) for the provider-specific parameters and requirements.


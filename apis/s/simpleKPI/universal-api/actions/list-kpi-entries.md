# SimpleKPI: List KPI Entries

Retrieves KPI entries from a SimpleKPI account.

```
GET https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-kpi-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-kpi-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-kpi-entries?${params}`, {
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
| `kpiId` | number | no | Optional SimpleKPI KPI ID filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual": 1,
      "addToActual": true,
      "created_at": "string",
      "email": "ava@example.com",
      "entry_date": "string",
      "id": 1,
      "kpi_id": 1,
      "notes": "string",
      "setActual": true,
      "setNotes": true,
      "setTarget": true,
      "target": "string",
      "updated_at": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual` | number |  |
| `addToActual` | boolean |  |
| `created_at` | string |  |
| `email` | string |  |
| `entry_date` | string |  |
| `id` | number |  |
| `kpi_id` | number |  |
| `notes` | string |  |
| `setActual` | boolean |  |
| `setNotes` | boolean |  |
| `setTarget` | boolean |  |
| `target` | string |  |
| `updated_at` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `GET kpientries` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-kpi-entries.md) for the provider-specific parameters and requirements.


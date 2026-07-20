# SimpleKPI: Create KPI Entry

Creates a new KPI entry in SimpleKPI.

```
POST https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-kpi-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-kpi-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-kpi-entry', {
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
| `actual` | number | no | The KPI actual value. |
| `addToActual` | boolean | no | Whether to add to the existing actual value. |
| `email` | string | no | The user email for the entry when user_id is not used. |
| `entry_date` | string | no | The KPI entry date in YYYY-MM-DD format. |
| `kpi_id` | number | no | The SimpleKPI KPI ID for the entry. |
| `notes` | string | no | Optional notes for the KPI entry. |
| `setActual` | boolean | no | Whether to set the actual value. |
| `setNotes` | boolean | no | Whether to set the notes value. |
| `setTarget` | boolean | no | Whether to set the target value. |
| `target` | number | no | The KPI target value. |
| `user_id` | number | no | The SimpleKPI user ID for the entry. |

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

Through the native SimpleKPI API, this operation is `POST kpientries` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-kpi-entry.md) for the provider-specific parameters and requirements.


# SimpleKPI: Create User KPI

Creates a KPI for a SimpleKPI user.

```
POST https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-user-kpi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-user-kpi" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-user-kpi', {
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
| `id` | number | no | The KPI ID to assign to the user. |
| `sort_order` | number | no | The display order of the KPI for the user. |
| `user_target` | number | no | An optional target override for the assigned KPI. |
| `userId` | number | no | The user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": 1,
      "sort_order": 1,
      "updated_at": "string",
      "user_id": 1,
      "user_target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | number |  |
| `sort_order` | number |  |
| `updated_at` | string |  |
| `user_id` | number |  |
| `user_target` | string |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `POST users/:userId/kpis` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-kpi.md) for the provider-specific parameters and requirements.


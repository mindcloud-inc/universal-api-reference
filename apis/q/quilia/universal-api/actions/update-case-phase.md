# Quilia: Update Case Phase



```
PUT https://connect.mindcloud.co/v1/universal/quilia/latest/actions/update-case-phase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quilia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/update-case-phase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "phase": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quilia/latest/actions/update-case-phase', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "phase": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cms_data` | string | no | Any additional custom data for the case |
| `id` | string | yes | The unique identifier of the case to update |
| `phase` | string | yes | The new phase for the case |
| `updated_at` | date | no | The date and time when the case was last updated (ISO 8601 format) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quilia API returns.

## Native endpoint

Through the native Quilia API, this operation is `PATCH cases/:id/phase` (base URL `https://api.quilia.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-case-phase.md) for the provider-specific parameters and requirements.


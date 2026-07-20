# Rachio Smart Hose Timer: Update Program V2

Updates an existing program in Rachio.

```
PUT https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/update-program-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/update-program-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/update-program-v2', {
  method: 'PUT',
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
| `id` | string | no |  |
| `name` | string | no |  |
| `color` | string | no |  |
| `enabled` | boolean | no |  |
| `dailyInterval` | object | no |  |
| `daysOfWeek` | object | no |  |
| `oddDays` | string | no |  |
| `evenDays` | string | no |  |
| `plannedRuns[]` | array<object> | no |  |
| `rainSkipEnabled` | boolean | no |  |
| `settings` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Hose Timer API returns.

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `PUT https://cloud-rest.rach.io/program/updateProgramV2` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-program-v2.md) for the provider-specific parameters and requirements.


# Rachio Smart Hose Timer: Create Program V2

Creates a new program in Rachio.

```
POST https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-program-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-program-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-program-v2', {
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
| `name` | string | no |  |
| `color` | string | no |  |
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

Through the native Rachio Smart Hose Timer API, this operation is `POST https://cloud-rest.rach.io/program/createProgramV2` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-program-v2.md) for the provider-specific parameters and requirements.


# Rachio Smart Hose Timer: Create Planned Run Skip Overrides

Creates planned run skip overrides in Rachio.

```
POST https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-planned-run-skip-overrides
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-planned-run-skip-overrides" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "plannedRunId": "string",
  "date": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-planned-run-skip-overrides', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "plannedRunId": "string",
    "date": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `plannedRunId` | string | yes |  |
| `date` | object | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Hose Timer API returns.

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `POST https://cloud-rest.rach.io/program/createPlannedRunSkipOverrides` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-planned-run-skip-overrides.md) for the provider-specific parameters and requirements.


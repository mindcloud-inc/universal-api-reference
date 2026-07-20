# EARLY: Create Leave

Creates a new leave in EARLY.

```
POST https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/create-leave
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EARLY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/create-leave" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "typeId": "1",
  "startDate": "2026-04-10T09:00:00.000",
  "endDate": "2026-04-10T17:00:00.000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/create-leave', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "typeId": "1",
    "startDate": "2026-04-10T09:00:00.000",
    "endDate": "2026-04-10T17:00:00.000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `typeId` | string | yes | Leave type ID. Default: `1`. |
| `startDate` | string | yes | Leave start timestamp. Default: `2026-04-10T09:00:00.000`. |
| `endDate` | string | yes | Leave end timestamp. Default: `2026-04-10T17:00:00.000`. |
| `note` | string | no | Optional leave note. Default: `MindCloud default leave test`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EARLY API returns.

## Native endpoint

Through the native EARLY API, this operation is `POST /api/v4/leaves` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-leave.md) for the provider-specific parameters and requirements.


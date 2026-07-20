# RunSignup: Create or Edit Race Corrals



```
PUT https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/create-or-edit-race-corrals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/create-or-edit-race-corrals" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "raceId": 1,
  "raceEventDaysId": 1,
  "request": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/create-or-edit-race-corrals', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "raceId": 1,
    "raceEventDaysId": 1,
    "request": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `raceId` | number | yes | Race ID. |
| `raceEventDaysId` | number | yes | Race event days ID. |
| `request` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `POST /v2/corrals/manage-corrals.json` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-edit-race-corrals.md) for the provider-specific parameters and requirements.


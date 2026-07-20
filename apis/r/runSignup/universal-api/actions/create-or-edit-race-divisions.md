# RunSignup: Create or Edit Race Divisions



```
PUT https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/create-or-edit-race-divisions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/create-or-edit-race-divisions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "raceId": 1,
  "eventId": 1,
  "request": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/create-or-edit-race-divisions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "raceId": 1,
    "eventId": 1,
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
| `eventId` | number | yes | Event ID. |
| `resultSetId` | number | no | Result set ID to associate with all divisions in the request. |
| `request` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `POST /v2/divisions/manage-divisions.json` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-edit-race-divisions.md) for the provider-specific parameters and requirements.


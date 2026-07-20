# RunSignup: Add or Edit Race Participants



```
PUT https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/add-or-edit-race-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/add-or-edit-race-participants" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "raceId": "string",
  "eventId": 1,
  "restrictPotentialDup": "string",
  "request": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/add-or-edit-race-participants', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "raceId": "string",
    "eventId": 1,
    "restrictPotentialDup": "string",
    "request": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `raceId` | string | yes | Path parameter: race_id |
| `eventId` | number | yes | ID of event. |
| `restrictPotentialDup` | string | yes |  |
| `clearNullCorrals` | string | no |  |
| `request` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `POST /race/:race_id/participants` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-or-edit-race-participants.md) for the provider-specific parameters and requirements.


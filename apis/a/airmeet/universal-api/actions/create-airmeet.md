# Airmeet: Create Airmeet

Creates a new event in Airmeet.

```
POST https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/create-airmeet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airmeet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/create-airmeet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventName": "Ava Chen",
  "hostEmail": "ava@example.com",
  "shortDesc": "string",
  "timing.endTime": 1,
  "timing.startTime": 1,
  "timing.timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/create-airmeet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventName": "Ava Chen",
    "hostEmail": "ava@example.com",
    "shortDesc": "string",
    "timing.endTime": 1,
    "timing.startTime": 1,
    "timing.timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventName` | string | yes | Name of the Airmeet event. |
| `hostEmail` | string | yes | Email address of the Airmeet event host. |
| `shortDesc` | string | yes | Short description of the event. |
| `timing.endTime` | number | yes | Event end time as a Unix timestamp in milliseconds. |
| `timing.startTime` | number | yes | Event start time as a Unix timestamp in milliseconds. |
| `timing.timezone` | string | yes | Canonical time zone name for the event. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airmeet API returns.

## Native endpoint

Through the native Airmeet API, this operation is `POST /airmeet` (base URL `https://api-gateway-prod.us.airmeet.com/prod`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-airmeet.md) for the provider-specific parameters and requirements.


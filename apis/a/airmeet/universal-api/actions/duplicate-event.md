# Airmeet: Duplicate Event

Creates a duplicate event in Airmeet.

```
POST https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/duplicate-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airmeet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/duplicate-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "airmeetId": "string",
  "eventName": "Ava Chen",
  "startTime": 1,
  "timeZone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/duplicate-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "airmeetId": "string",
    "eventName": "Ava Chen",
    "startTime": 1,
    "timeZone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `airmeetId` | string | yes | The source Airmeet event ID to duplicate. |
| `duplicateSpeakers` | boolean | no | Set true to include the original event speakers in the duplicate. |
| `eventName` | string | yes | Name for the duplicate event. |
| `startTime` | number | yes | Start time for the duplicate event as a Unix timestamp in milliseconds. |
| `timeZone` | string | yes | Canonical time zone name for the duplicate event. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airmeet API returns.

## Native endpoint

Through the native Airmeet API, this operation is `POST /airmeet/{airmeetId}/duplication` (base URL `https://api-gateway-prod.us.airmeet.com/prod`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-event.md) for the provider-specific parameters and requirements.


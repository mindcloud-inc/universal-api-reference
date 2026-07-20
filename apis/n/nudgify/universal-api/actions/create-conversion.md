# Nudgify: Create Conversion

Creates conversion events in Nudgify.

```
POST https://connect.mindcloud.co/v1/universal/nudgify/latest/actions/create-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nudgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nudgify/latest/actions/create-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversions[]": [
    {}
  ],
  "conversions[].date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nudgify/latest/actions/create-conversion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversions[]": [{}],
    "conversions[].date": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversions[]` | array<object> | yes | One or more conversion events to send to Nudgify. |
| `conversions[].date` | string | yes | UTC timestamp in `Y-m-d H:i:s` format. |
| `conversions[].email` | string | no | Email address tied to the conversion. |
| `conversions[].firstName` | string | no | First name to show in the nudge. |
| `conversions[].lastName` | string | no | Last name to show in the nudge. |
| `conversions[].ip` | string | no | IP address used for location fallback. |
| `conversions[].city` | string | no | City to show in the nudge. |
| `conversions[].state` | string | no | State or region to show in the nudge. |
| `conversions[].country` | string | no | ISO 3166-1 alpha-2 country code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nudgify API returns.

## Native endpoint

Through the native Nudgify API, this operation is `POST /api/conversions` (base URL `https://app.nudgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversion.md) for the provider-specific parameters and requirements.


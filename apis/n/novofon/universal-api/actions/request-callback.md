# Novofon: Request Callback

Creates a callback request in Novofon.

```
POST https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-callback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novofon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-callback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-callback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Your phone number, SIP, or PBX internal number that receives the callback. |
| `predicted` | string | no | Optional provider flag for predictive callback behavior. Pass the provider-accepted truthy value when needed. |
| `sip` | string | no | Optional SIP user number or PBX internal number used to place the call. |
| `to` | string | yes | Phone number or SIP destination to call. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Novofon API returns.

## Native endpoint

Through the native Novofon API, this operation is `GET /v1/request/callback/` (base URL `https://api.novofon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-callback.md) for the provider-specific parameters and requirements.


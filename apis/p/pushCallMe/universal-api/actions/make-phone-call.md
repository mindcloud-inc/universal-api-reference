# PushCallMe: Make Phone Call

Creates a new phone call in PushCallMe.

```
POST https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/make-phone-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PushCallMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/make-phone-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/make-phone-call', {
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
| `from` | string | yes | Caller selector. PushCall's docs describe this as a caller ID index, while provided webhook examples may use a full caller number. |
| `to` | string<string> | yes | Destination phone number to call. PushCall's docs also mention repeating the `to` query parameter for multiple recipients, but this draft currently keeps the single-recipient contract until repeated query values can be modeled cleanly in runtime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "from": "string",
      "message": "string",
      "requestId": "string",
      "success": true,
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from` | string | Caller number used for the call. |
| `message` | string | PushCall confirmation message. |
| `requestId` | string | Request identifier used to look up the eventual call result. |
| `success` | boolean | Whether PushCall accepted the call request. |
| `to` | string | Destination number that was called. |

## Native endpoint

Through the native PushCallMe API, this operation is `GET /api/call` (base URL `https://pushcall.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/make-phone-call.md) for the provider-specific parameters and requirements.


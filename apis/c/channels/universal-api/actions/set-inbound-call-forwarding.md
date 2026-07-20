# Channels: Set Inbound Call Forwarding

Updates inbound call forwarding for a phone number in Channels.

```
PUT https://connect.mindcloud.co/v1/universal/channels/latest/actions/set-inbound-call-forwarding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channels/latest/actions/set-inbound-call-forwarding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msisdnId": 1,
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channels/latest/actions/set-inbound-call-forwarding', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msisdnId": 1,
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msisdnId` | number | yes | Phone number ID whose forwarding configuration should be updated. |
| `phoneNumber` | string | yes | Phone number where incoming calls should be forwarded. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Channels API, this operation is `POST /api/v1/inbound/configuration/numbers/{msisdnId}/forward` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-inbound-call-forwarding.md) for the provider-specific parameters and requirements.


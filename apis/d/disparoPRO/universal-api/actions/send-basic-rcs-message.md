# Disparo PRO: Send Basic RCS Message

Creates a basic RCS message in Disparo PRO.

```
POST https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/send-basic-rcs-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Disparo PRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/send-basic-rcs-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/send-basic-rcs-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | Basic text message body. |
| `templateId` | string | no | Registered template ID. |
| `variables` | object | no | Variables mapping for the selected template. |
| `to` | string | yes | Recipient phone number in E.164 format. |
| `partnerData` | object | no | Additional integration data returned in webhooks. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Disparo PRO API returns.

## Native endpoint

Through the native Disparo PRO API, this operation is `POST /message/basic` (base URL `https://gateway.disparopro.com.br/rcs`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-basic-rcs-message.md) for the provider-specific parameters and requirements.


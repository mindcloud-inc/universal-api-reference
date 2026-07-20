# Disparo PRO: Send Single RCS Message

Creates a single RCS message in Disparo PRO.

```
POST https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/send-single-rcs-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Disparo PRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/send-single-rcs-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "variables": {},
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/send-single-rcs-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "variables": {},
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Registered template ID. |
| `variables` | object | yes | Variables mapping for the selected template. |
| `to` | string | yes | Recipient phone number in E.164 format. |
| `partnerData` | object | no | Additional integration data returned in webhooks. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Disparo PRO API returns.

## Native endpoint

Through the native Disparo PRO API, this operation is `POST /message/single` (base URL `https://gateway.disparopro.com.br/rcs`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-single-rcs-message.md) for the provider-specific parameters and requirements.


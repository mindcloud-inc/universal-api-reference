# Clicksign: Create Signer

Creates a signer in a Clicksign envelope.

```
POST https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clicksign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-signer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.attributes.email": "ava@example.com",
  "data.attributes.name": "Ava Chen",
  "envelopeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-signer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.attributes.email": "ava@example.com",
    "data.attributes.name": "Ava Chen",
    "envelopeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | JSON:API document wrapper. |
| `data.attributes` | object | no | Signer attributes. |
| `data.attributes.birthday` | date | no | The signer birth date. |
| `data.attributes.communicateEvents` | object | no | Notification channel settings. |
| `data.attributes.communicateEvents.documentSigned` | string | no | Delivery channel for signed-document notices. |
| `data.attributes.communicateEvents.signatureReminder` | string | no | Delivery channel for signature reminders. |
| `data.attributes.communicateEvents.signatureRequest` | string | no | Delivery channel for signature requests. |
| `data.attributes.documentation` | string | no | The signer documentation number. |
| `data.attributes.email` | string | yes | The signer email address. |
| `data.attributes.group` | number | no | The signer group number. |
| `data.attributes.hasDocumentation` | boolean | no | Whether signer documentation is provided. |
| `data.attributes.locationRequiredEnabled` | boolean | no | Whether signer geolocation is required. |
| `data.attributes.name` | string | yes | The signer name. |
| `data.attributes.phoneNumber` | string | no | The signer phone number. |
| `data.attributes.refusable` | boolean | no | Whether the signer can refuse. |
| `envelopeId` | string | yes | The UUID of the envelope. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clicksign API returns.

## Native endpoint

Through the native Clicksign API, this operation is `POST /envelopes/:envelope_id/signers` (base URL `https://app.clicksign.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signer.md) for the provider-specific parameters and requirements.


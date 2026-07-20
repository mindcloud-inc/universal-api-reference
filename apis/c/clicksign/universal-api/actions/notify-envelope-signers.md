# Clicksign: Notify Envelope Signers

Notifies signers for a Clicksign envelope.

```
POST https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/notify-envelope-signers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clicksign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/notify-envelope-signers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "envelopeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/notify-envelope-signers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `envelopeId` | string | yes | The UUID of the envelope. |
| `data.attributes` | object | no | Notification attributes. |
| `data.attributes.message` | string | no | Message sent to the signer. If omitted, Clicksign uses the envelope default message. |
| `data.attributes.emailCustomization` | object | no | Custom email notification settings. |
| `data.attributes.emailCustomization.subject` | string | no | Custom email subject. |
| `data.attributes.emailCustomization.head` | string | no | Custom email header text. |
| `data.attributes.emailCustomization.greeting` | string | no | Custom email greeting. |
| `data.attributes.emailCustomization.principal` | string | no | Custom main email message. |
| `data.attributes.emailCustomization.button` | string | no | Custom button label in the email. |
| `data.attributes.emailCustomization.final` | string | no | Custom final email message after the button. |
| `data.attributes.emailCustomization.align` | string | no | Email content alignment. |
| `data.attributes.emailCustomization.showToken` | boolean | no | Whether to show the token in the email body when token authentication exists. |
| `data.attributes.emailCustomization.showQrcode` | boolean | no | Whether to include a QR code pointing to the signing link. |
| `data.attributes.emailCustomization.showDetails` | boolean | no | Whether to show signature-process details in the email. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clicksign API returns.

## Native endpoint

Through the native Clicksign API, this operation is `POST /envelopes/:envelope_id/notifications` (base URL `https://app.clicksign.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/notify-envelope-signers.md) for the provider-specific parameters and requirements.


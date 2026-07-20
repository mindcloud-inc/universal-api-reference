# Routee: Send a Viber Verification Message (OTP)

Sends a Viber verification message (OTP) with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-viber-verification-message-otp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-viber-verification-message-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "senderInfoTrackingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-viber-verification-message-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "senderInfoTrackingId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderInfoTrackingId` | string | yes | Unique identifier of the Viber sender (from your sender configuration). Used for routing and tracking |
| `to[]` | array<string> | no | Recipient phone number in **E.164** format (e.g. `+306912345678`). Must include `+` and country code |
| `ttl` | number | no | Time-to-live in **seconds** for the OTP delivery attempt |
| `seq` | string | no | Your own sequence or correlation ID for this request (e.g. for linking request and response or callbacks) |
| `label` | string | no | Message label. Allowed values: `transactional`, `promotional` |
| `type` | string | no | OTP message type. Allowed values: `PRIMARY_ONLY`, `ALL_DEVICE` |
| `templateId` | string | no | ID of the OTP template to use. See [Templates inventory](https://docs.routee.net/docs/templates-inventory) |
| `templateParams` | object | no | Key-value map of template variables. Keys in **camelCase** (e.g. `pin`, `businessPlatformName`, `codeValidityTime`). See [Template variables validation](https://docs.routee.net/docs/template-variables-validations) |
| `templateLang` | string | no | Language of the template (ISO 639-1, e.g. `en`, `el`). See [Localization](https://docs.routee.net/docs/localization) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationName": "Ava Chen",
      "country": "string",
      "direction": "string",
      "from": "string",
      "label": "string",
      "seq": 1,
      "status": {
        "date": "string",
        "status": "string"
      },
      "templateId": "string",
      "templateLang": "string",
      "templateParams": {
        "pin": "string"
      },
      "to": "string",
      "trackingId": "string",
      "ttl": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationName` | string |  |
| `country` | string |  |
| `direction` | string |  |
| `from` | string |  |
| `label` | string |  |
| `seq` | number |  |
| `status` | object |  |
| `status.date` | string |  |
| `status.status` | string |  |
| `templateId` | string |  |
| `templateLang` | string |  |
| `templateParams` | object |  |
| `templateParams.pin` | string |  |
| `to` | string |  |
| `trackingId` | string |  |
| `ttl` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /viber/otp` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-a-viber-verification-message-otp.md) for the provider-specific parameters and requirements.


# WhatsBoost: Validate a WhatsApp phone number

Validates a WhatsApp phone number in WhatsBoost.

```
GET https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/validate-a-whats-app-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBoost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/validate-a-whats-app-phone-number?connectionId=$CONNECTION_ID&unique=string&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "unique": "string",
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/validate-a-whats-app-phone-number?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `unique` | string | yes | WhatsApp Unique ID |
| `phone` | string | yes | E.164 formatted phone number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native WhatsBoost API, this operation is `POST /validate/whatsapp` (base URL `https://whatsboost.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-a-whats-app-phone-number.md) for the provider-specific parameters and requirements.


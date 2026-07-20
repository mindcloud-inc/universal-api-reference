# WhatsScale: Check WhatsApp Number

Checks whether a phone number uses WhatsApp via WhatsScale.

```
GET https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/check-whats-app-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/check-whats-app-number?connectionId=$CONNECTION_ID&phone=string&session=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string",
  "session": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/check-whats-app-number?${params}`, {
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
| `phone` | string | yes | Phone number to check. |
| `session` | string | yes | Session name from /api/sessions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chatId": "string",
      "numberExists": true,
      "phone": "string",
      "phoneFormatted": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatId` | string |  |
| `numberExists` | boolean |  |
| `phone` | string |  |
| `phoneFormatted` | string |  |

## Native endpoint

Through the native WhatsScale API, this operation is `POST /api/checkWhatsapp` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-whats-app-number.md) for the provider-specific parameters and requirements.


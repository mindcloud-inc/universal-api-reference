# 2Chat: Check If Number Is On WhatsApp

Finds whether a phone number is on WhatsApp in 2Chat.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/check-if-number-is-on-whats-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/check-if-number-is-on-whats-app?connectionId=$CONNECTION_ID&from_number=string&number_to_check=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from_number": "string",
  "number_to_check": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/check-if-number-is-on-whats-app?${params}`, {
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
| `from_number` | string | yes | The WhatsApp number connected to 2Chat that performs the check. |
| `number_to_check` | string | yes | The phone number to verify on WhatsApp. |
| `extraInformation` | boolean | no | Include extended WhatsApp profile information when available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isValid": true,
      "number": {
        "carrier": "string",
        "e164Format": "string",
        "isoCountryCode": "string",
        "region": "string",
        "timezone": [
          "string"
        ]
      },
      "onWhatsapp": true,
      "whatsappInfo": {
        "numberId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isValid` | boolean |  |
| `number.carrier` | string |  |
| `number.e164Format` | string |  |
| `number.isoCountryCode` | string |  |
| `number.region` | string |  |
| `number.timezone[]` | string |  |
| `onWhatsapp` | boolean |  |
| `whatsappInfo.numberId` | string |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /whatsapp/check-number/:from_number/:number_to_check` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-if-number-is-on-whats-app.md) for the provider-specific parameters and requirements.


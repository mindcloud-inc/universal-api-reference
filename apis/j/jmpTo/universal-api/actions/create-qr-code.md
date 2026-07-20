# JmpTo: Create QR Code

Creates a QR code in JmpTo.

```
POST https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "data": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "data": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `background` | string | no | Background RGB color. |
| `foreground` | string | no | Foreground RGB color. |
| `logo` | string | no | Path to a PNG or JPG logo. |
| `type` | string | yes | QR code type: text, vcard, link, email, phone, sms, or wifi. |
| `data` | string | yes | Data to embed in the QR code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "id": "string",
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number | Provider success/error code. |
| `id` | string | QR code ID returned by the provider. |
| `link` | string | Generated QR code link. |

## Native endpoint

Through the native JmpTo API, this operation is `POST /qr/add` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-qr-code.md) for the provider-specific parameters and requirements.


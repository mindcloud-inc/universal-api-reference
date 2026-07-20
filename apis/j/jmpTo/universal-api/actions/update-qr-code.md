# JmpTo: Update QR Code

Updates an existing QR code in JmpTo.

```
PUT https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "data": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-qr-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
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
| `id` | number | yes | QR code ID to update. |
| `logo` | string | no | Path to a PNG or JPG logo. |
| `data` | string | yes | Data to embed in the QR code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number | Provider success/error code. |
| `message` | string | Update result message. |

## Native endpoint

Through the native JmpTo API, this operation is `PUT /qr/:id/update` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-qr-code.md) for the provider-specific parameters and requirements.


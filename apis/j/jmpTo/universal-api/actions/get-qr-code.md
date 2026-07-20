# JmpTo: Get QR Code

Retrieves a QR code from JmpTo.

```
GET https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-qr-code?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-qr-code?${params}`, {
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
| `id` | number | yes | QR code ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "id": 1,
      "link": "https://example.com",
      "name": "Ava Chen",
      "scans": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Provider timestamp value returned for the QR code. |
| `id` | number | QR code ID. |
| `link` | string | Generated QR code URL. |
| `name` | string | QR code name. |
| `scans` | number | Scan count. |

## Native endpoint

Through the native JmpTo API, this operation is `GET /qr/:id` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qr-code.md) for the provider-specific parameters and requirements.


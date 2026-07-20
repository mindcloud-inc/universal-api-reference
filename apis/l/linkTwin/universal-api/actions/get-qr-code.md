# LinkTwin: Get QR Code

Retrieves a QR code from LinkTwin.

```
GET https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-qr-code?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-qr-code?${params}`, {
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
| `id` | string | yes | Example: `1`. |

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
| `error` | number |  |
| `message` | string |  |

## Native endpoint

Through the native LinkTwin API, this operation is `GET /qr/:id` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qr-code.md) for the provider-specific parameters and requirements.


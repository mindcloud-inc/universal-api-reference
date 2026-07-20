# Recut URL Shortener: Delete QR Code

Deletes an existing QR code from Recut URL Shortener.

```
DELETE https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/delete-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/delete-qr-code?connectionId=$CONNECTION_ID&id=843" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "843"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/delete-qr-code?${params}`, {
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
| `id` | number | yes | QR code ID Example: `843`. |

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

Through the native Recut URL Shortener API, this operation is `DELETE /qr/:id/delete` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-qr-code.md) for the provider-specific parameters and requirements.


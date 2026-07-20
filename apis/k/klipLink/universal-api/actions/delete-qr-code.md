# KlipLink: Delete QR Code



```
DELETE https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/delete-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KlipLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/delete-qr-code?connectionId=$CONNECTION_ID&shortUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/delete-qr-code?${params}`, {
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
| `shortUrl` | string | yes | The short URL identifier, for example klipl.ink/example. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KlipLink API returns.

## Native endpoint

Through the native KlipLink API, this operation is `DELETE /v1/qrcodes/:short_url` (base URL `https://api.klipl.ink`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-qr-code.md) for the provider-specific parameters and requirements.


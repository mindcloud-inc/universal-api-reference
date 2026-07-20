# Scanova: Download QR Code (Printable)



```
GET https://connect.mindcloud.co/v1/universal/scanova/latest/actions/download-qr-code-printable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/download-qr-code-printable?connectionId=$CONNECTION_ID&qrid=string&forPrint=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "qrid": "string",
  "forPrint": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scanova/latest/actions/download-qr-code-printable?${params}`, {
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
| `qrid` | string | yes | QR code ID |
| `name` | string | no | Name for the downloaded file |
| `forPrint` | string | yes | Must be set to 'true' for printable format |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `size` | string | no | Size of the QR code in pixels (300-600px) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scanova API returns.

## Native endpoint

Through the native Scanova API, this operation is `POST /qr/download/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-qr-code-printable.md) for the provider-specific parameters and requirements.


# Qryptal: Generate EDC QR Code With Attachments



```
POST https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/generate-edc-qr-code-with-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qryptal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/generate-edc-qr-code-with-attachments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/generate-edc-qr-code-with-attachments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | string | yes | JSON string containing the Qryptal payload with data, format, and scheme. Example: `[object Object]`. |
| `img1` | file | no | Optional image attachment for the multipart field named img1. |
| `file1` | file | no | Optional document attachment for the multipart field named file1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apitype": "string",
      "codeToken": "string",
      "ct": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "msg": "string",
      "qrText": "string",
      "qrurl": "https://example.com",
      "scheme": "string",
      "status": "string",
      "uid": "string",
      "vqtype": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apitype` | string | Qryptal API operation type returned by the service. |
| `codeToken` | string | Token required for later QR image download and lifecycle operations. |
| `ct` | date | Creation timestamp returned by Qryptal. |
| `id` | number | Qryptal internal record identifier. |
| `msg` | string | Human-readable Qryptal status message. |
| `qrText` | string | Raw QR payload text returned by Qryptal. |
| `qrurl` | string | Direct URL for downloading the generated QR image. |
| `scheme` | string | QR scheme returned by Qryptal. |
| `status` | string | Creation status code such as P, C, or E. |
| `uid` | string | Stable Qryptal unique identifier for the created code. |
| `vqtype` | string | Qryptal code type, for example PDC or TEDC. |

## Native endpoint

Through the native Qryptal API, this operation is `POST /` (base URL `https://api2test.qryptal.com/v2/Vqodes/v2/Vqodes/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-edc-qr-code-with-attachments.md) for the provider-specific parameters and requirements.


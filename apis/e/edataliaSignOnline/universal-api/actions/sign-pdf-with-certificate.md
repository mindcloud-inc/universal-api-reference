# edatalia Sign Online: Sign PDF With Certificate

Signs a PDF with a certificate in edatalia Sign Online.

```
POST https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/sign-pdf-with-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a edatalia Sign Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/sign-pdf-with-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "b64PDFContent": "string",
  "widget": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/sign-pdf-with-certificate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "b64PDFContent": "string",
    "widget": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `b64PDFContent` | string | yes | PDF document content encoded as base64. |
| `widget` | object | yes | Signature widget definition. The API supports fixed, floating, or field-based widget shapes. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `certificate` | object | no | Optional signing certificate information. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Signed PDF content returned by the API. |

## Native endpoint

Through the native edatalia Sign Online API, this operation is `POST /eSign/v40/Signature` (base URL `https://restapi.firmar.online`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sign-pdf-with-certificate.md) for the provider-specific parameters and requirements.


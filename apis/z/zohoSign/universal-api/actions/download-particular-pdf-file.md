# Zoho Sign: Download Particular PDF File

Downloads a particular PDF file from Zoho Sign.

```
GET https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/download-particular-pdf-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/download-particular-pdf-file?connectionId=$CONNECTION_ID&requestId=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/download-particular-pdf-file?${params}`, {
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
| `requestId` | string | yes | Zoho Sign request identifier. |
| `documentId` | string | yes | Zoho Sign document identifier inside the request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `GET /requests/:requestId/documents/:documentId/pdf` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-particular-pdf-file.md) for the provider-specific parameters and requirements.


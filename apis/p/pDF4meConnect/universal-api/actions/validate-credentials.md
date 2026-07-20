# PDF4me Connect: Validate Credentials



```
GET https://connect.mindcloud.co/v1/universal/pDF4meConnect/latest/actions/validate-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF4me Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDF4meConnect/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDF4meConnect/latest/actions/validate-credentials?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "documentId": "string",
      "isEncrypted": true,
      "isLinearized": true,
      "isSigned": true,
      "keywords": "string",
      "modDate": "2026-05-07T12:00:00.000Z",
      "orientation": "string",
      "pageCount": 1,
      "pageHeightInMM": 1,
      "pageWidthInMM": 1,
      "pdfCompliance": "string",
      "pdfVersion": "string",
      "producer": "string",
      "size": 1,
      "subject": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `creationDate` | date |  |
| `creator` | string |  |
| `documentId` | string |  |
| `isEncrypted` | boolean |  |
| `isLinearized` | boolean |  |
| `isSigned` | boolean |  |
| `keywords` | string |  |
| `modDate` | date |  |
| `orientation` | string |  |
| `pageCount` | number |  |
| `pageHeightInMM` | number |  |
| `pageWidthInMM` | number |  |
| `pdfCompliance` | string |  |
| `pdfVersion` | string |  |
| `producer` | string |  |
| `size` | number |  |
| `subject` | string |  |
| `title` | string |  |

## Native endpoint

Through the native PDF4me Connect API, this operation is `POST /api/v2/GetPdfMetadata` (base URL `https://api.pdf4me.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-credentials.md) for the provider-specific parameters and requirements.


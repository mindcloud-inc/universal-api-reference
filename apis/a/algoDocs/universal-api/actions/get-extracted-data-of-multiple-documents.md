# AlgoDocs: Get Extracted Data of Multiple Documents

Retrieves extracted data from AlgoDocs documents by extractor.

```
GET https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/get-extracted-data-of-multiple-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AlgoDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/get-extracted-data-of-multiple-documents?connectionId=$CONNECTION_ID&extractorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extractorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/get-extracted-data-of-multiple-documents?${params}`, {
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
| `extractorId` | string | yes | The extractor ID from your AlgoDocs account. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | no | Optional folder filter for extracted data results. |
| `date` | string | no | Optional ISO 8601 date filter for documents uploaded after this date. Example: `2017-06-21T10:45:52`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "documentId": 1,
      "fileName": "Ava Chen",
      "folderId": "string",
      "id": "string",
      "mediaExcel": "string",
      "mediaJson": "string",
      "mediaOriginal": "string",
      "mediaXml": "string",
      "pageNumber": 1,
      "processedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "totalPages": 1,
      "uploadedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `documentId` | number |  |
| `fileName` | string |  |
| `folderId` | string |  |
| `id` | string |  |
| `mediaExcel` | string |  |
| `mediaJson` | string |  |
| `mediaOriginal` | string |  |
| `mediaXml` | string |  |
| `pageNumber` | number |  |
| `processedAt` | date |  |
| `status` | string |  |
| `totalPages` | number |  |
| `uploadedAt` | date |  |

## Native endpoint

Through the native AlgoDocs API, this operation is `GET /extracted_data/:extractorId` (base URL `https://api.algodocs.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extracted-data-of-multiple-documents.md) for the provider-specific parameters and requirements.


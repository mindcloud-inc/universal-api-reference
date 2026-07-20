# TalentHR: List Company Documents

Retrieves company documents from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-company-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-company-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-company-documents?${params}`, {
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
      "aiSummary": "string",
      "aiSummaryError": "string",
      "clientFilename": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "documentType": "string",
      "expirationId": 1,
      "filename": "Ava Chen",
      "filesize": 1,
      "filetype": "string",
      "folderId": 1,
      "id": 1,
      "isEmployeeFile": true,
      "isFolder": true,
      "isPublic": true,
      "masterId": 1,
      "nonSignedFilename": "Ava Chen",
      "ownerId": 1,
      "previewFilename": "Ava Chen",
      "previewUrl": "https://example.com",
      "signingFinalizedAt": "2026-05-07T12:00:00.000Z",
      "signingStartedAt": "2026-05-07T12:00:00.000Z",
      "sortOrder": 1,
      "starred": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uploadedId": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiSummary` | string |  |
| `aiSummaryError` | string |  |
| `clientFilename` | string |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `documentType` | string |  |
| `expirationId` | number |  |
| `filename` | string |  |
| `filesize` | number |  |
| `filetype` | string |  |
| `folderId` | number |  |
| `id` | number |  |
| `isEmployeeFile` | boolean |  |
| `isFolder` | boolean |  |
| `isPublic` | boolean |  |
| `masterId` | number |  |
| `nonSignedFilename` | string |  |
| `ownerId` | number |  |
| `previewFilename` | string |  |
| `previewUrl` | string |  |
| `signingFinalizedAt` | date |  |
| `signingStartedAt` | date |  |
| `sortOrder` | number |  |
| `starred` | boolean |  |
| `updatedAt` | date |  |
| `uploadedId` | number |  |
| `url` | string |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /documents/company-documents` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-documents.md) for the provider-specific parameters and requirements.


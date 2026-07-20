# TalentHR: List Employee Documents

Retrieves an employee's documents from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-documents?connectionId=$CONNECTION_ID&employee=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employee": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-documents?${params}`, {
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
| `employee` | number | yes | TalentHR employee ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientFilename": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "filetype": "string",
      "id": 1,
      "isEmployeeFile": true,
      "isPublic": true,
      "masterId": 1,
      "ownerId": 1,
      "previewFilename": "Ava Chen",
      "previewUrl": "https://example.com",
      "sortOrder": 1,
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
| `clientFilename` | string |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `filename` | string |  |
| `filetype` | string |  |
| `id` | number |  |
| `isEmployeeFile` | boolean |  |
| `isPublic` | boolean |  |
| `masterId` | number |  |
| `ownerId` | number |  |
| `previewFilename` | string |  |
| `previewUrl` | string |  |
| `sortOrder` | number |  |
| `updatedAt` | date |  |
| `uploadedId` | number |  |
| `url` | string |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /employees/:employee/documents` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-documents.md) for the provider-specific parameters and requirements.


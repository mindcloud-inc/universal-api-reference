# Testlify: List Assessments

Retrieves assessments from Testlify with optional filters and pagination.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-assessments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-assessments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-assessments?${params}`, {
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
| `query` | string | no | Search query string. |
| `groupName` | string | no | Group name to filter assessments. |
| `workspaceLabelTitle` | string | no | Workspace label title. |
| `isActive` | boolean | no | Filter active assessments. |
| `isArchived` | boolean | no | Filter archived assessments. |
| `isEditable` | boolean | no | Filter editable assessments. |
| `isDraft` | boolean | no | Filter draft assessments. |
| `sortBy` | string | no | Column name to sort by. |
| `sortOrder` | string | no | Sort order. |
| `limit` | number | no | Number of items to return. |
| `skip` | number | no | Number of items to skip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessmentId": "string",
      "assessmentStatus": "string",
      "assessmentTitle": "string",
      "created": "string",
      "createdBy": "string",
      "groupName": "Ava Chen",
      "isArchived": true,
      "jobRoleId": "string",
      "publicInviteLink": "https://example.com",
      "totalCandidateCount": 1,
      "totalCompleted": 1,
      "totalInProgress": 1,
      "totalInvited": 1,
      "totalRejected": 1,
      "userId": "string",
      "workspaceLabel": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assessmentId` | string |  |
| `assessmentStatus` | string |  |
| `assessmentTitle` | string |  |
| `created` | string |  |
| `createdBy` | string |  |
| `groupName` | string |  |
| `isArchived` | boolean |  |
| `jobRoleId` | string |  |
| `publicInviteLink` | string |  |
| `totalCandidateCount` | number |  |
| `totalCompleted` | number |  |
| `totalInProgress` | number |  |
| `totalInvited` | number |  |
| `totalRejected` | number |  |
| `userId` | string |  |
| `workspaceLabel` | array<string> |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/assessment` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assessments.md) for the provider-specific parameters and requirements.


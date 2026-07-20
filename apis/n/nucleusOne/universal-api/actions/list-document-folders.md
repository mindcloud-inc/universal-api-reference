# Nucleus One: List Document Folders

Retrieves document folders from a Nucleus One project.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-document-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-document-folders?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-document-folders?${params}`, {
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
| `organizationId` | string | yes | ID of the organization Example: `Enter organizationId`. |
| `projectId` | string | yes | ID of the project Example: `Enter projectId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "AncestorAssignmentUserEmails": [
        "ava@example.com"
      ],
      "AncestorIDs": [
        "string"
      ],
      "AssignmentUserEmails": [
        "ava@example.com"
      ],
      "CreatedByUserEmail": "ava@example.com",
      "CreatedByUserID": "string",
      "CreatedByUserName": "Ava Chen",
      "CreatedByWorkflow": true,
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "Depth": 1,
      "HexColor": "string",
      "ID": "string",
      "ModifiedByUserEmail": "ava@example.com",
      "ModifiedByUserID": "string",
      "ModifiedByUserName": "Ava Chen",
      "ModifiedOn": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "NameLower": "Ava Chen",
      "OrganizationID": "string",
      "ParentID": "string",
      "ProjectAccess": {},
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "UniqueID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `AncestorAssignmentUserEmails` | array<string> |  |
| `AncestorIDs` | array<string> |  |
| `AssignmentUserEmails` | array<string> |  |
| `CreatedByUserEmail` | string |  |
| `CreatedByUserID` | string |  |
| `CreatedByUserName` | string |  |
| `CreatedByWorkflow` | boolean |  |
| `CreatedOn` | date |  |
| `Depth` | number |  |
| `HexColor` | string |  |
| `ID` | string |  |
| `ModifiedByUserEmail` | string |  |
| `ModifiedByUserID` | string |  |
| `ModifiedByUserName` | string |  |
| `ModifiedOn` | date |  |
| `Name` | string |  |
| `NameLower` | string |  |
| `OrganizationID` | string |  |
| `ParentID` | string |  |
| `ProjectAccess` | object |  |
| `ProjectID` | string |  |
| `ProjectName` | string |  |
| `UniqueID` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/documentFolders` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-folders.md) for the provider-specific parameters and requirements.


# Nucleus One: List Recycle Bin Documents

Retrieves recycle bin documents from a Nucleus One project.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-recycle-bin-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-recycle-bin-documents?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-recycle-bin-documents?${params}`, {
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
| `organizationId` | string | yes | organizationId path parameter. Example: `Enter organizationId`. |
| `projectId` | string | yes | projectId path parameter. Example: `Enter projectId`. |
| `projectId` | string | yes | projectId path parameter. Example: `Enter projectId`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor Example: `Paste a cursor from a previous response`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "ApprovalCreatedOn": "2026-05-07T12:00:00.000Z",
      "ApprovalID": "string",
      "AssetItemTags": [
        {}
      ],
      "AssignmentUserEmails": [
        "ava@example.com"
      ],
      "CreatedByUserEmail": "ava@example.com",
      "CreatedByUserID": "string",
      "CreatedByUserName": "Ava Chen",
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "DocumentFolderHexColor": "string",
      "DocumentFolderID": "string",
      "DocumentFolderPath": "string",
      "DocumentID": "string",
      "DocumentSubscriptionCreatedOn": "2026-05-07T12:00:00.000Z",
      "DocumentSubscriptionID": "string",
      "FileSize": 1,
      "FormSubmissionID": "string",
      "GroupID": "string",
      "HasSinglePageImages": true,
      "ID": "string",
      "IsMarkedForPurge": true,
      "IsSigned": true,
      "ModifiedByUserEmail": "ava@example.com",
      "ModifiedByUserID": "string",
      "ModifiedByUserName": "Ava Chen",
      "ModifiedOn": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "OrganizationID": "string",
      "Origin": "string",
      "PageCount": 1,
      "PaperMarginBottom": 1,
      "PaperMarginLeft": 1,
      "PaperMarginRight": 1,
      "PaperMarginTop": 1,
      "PaperOrientation": "string",
      "PaperSize": "string",
      "PreviewMetadata": [
        {}
      ],
      "ProcessElementName": "Ava Chen",
      "ProcessName": "Ava Chen",
      "ProjectAccess": {},
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "PurgeDate": "2026-05-07T12:00:00.000Z",
      "Revision": 1,
      "SignaturesCompletedOn": "2026-05-07T12:00:00.000Z",
      "SignatureSessionIsActive": true,
      "SyncDocumentID": "string",
      "SyncProjectName": "Ava Chen",
      "Tags": [
        "string"
      ],
      "ThumbnailUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `ApprovalCreatedOn` | date |  |
| `ApprovalID` | string |  |
| `AssetItemTags` | array<object> |  |
| `AssignmentUserEmails` | array<string> |  |
| `CreatedByUserEmail` | string |  |
| `CreatedByUserID` | string |  |
| `CreatedByUserName` | string |  |
| `CreatedOn` | date |  |
| `DocumentFolderHexColor` | string |  |
| `DocumentFolderID` | string |  |
| `DocumentFolderPath` | string |  |
| `DocumentID` | string |  |
| `DocumentSubscriptionCreatedOn` | date |  |
| `DocumentSubscriptionID` | string |  |
| `FileSize` | number |  |
| `FormSubmissionID` | string |  |
| `GroupID` | string |  |
| `HasSinglePageImages` | boolean |  |
| `ID` | string |  |
| `IsMarkedForPurge` | boolean |  |
| `IsSigned` | boolean |  |
| `ModifiedByUserEmail` | string |  |
| `ModifiedByUserID` | string |  |
| `ModifiedByUserName` | string |  |
| `ModifiedOn` | date |  |
| `Name` | string |  |
| `OrganizationID` | string |  |
| `Origin` | string |  |
| `PageCount` | number |  |
| `PaperMarginBottom` | number |  |
| `PaperMarginLeft` | number |  |
| `PaperMarginRight` | number |  |
| `PaperMarginTop` | number |  |
| `PaperOrientation` | string |  |
| `PaperSize` | string |  |
| `PreviewMetadata` | array<object> |  |
| `ProcessElementName` | string |  |
| `ProcessName` | string |  |
| `ProjectAccess` | object |  |
| `ProjectID` | string |  |
| `ProjectName` | string |  |
| `PurgeDate` | date |  |
| `Revision` | number |  |
| `SignaturesCompletedOn` | date |  |
| `SignatureSessionIsActive` | boolean |  |
| `SyncDocumentID` | string |  |
| `SyncProjectName` | string |  |
| `Tags` | array<string> |  |
| `ThumbnailUrl` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/recycleBinDocuments` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recycle-bin-documents.md) for the provider-specific parameters and requirements.


# Nucleus One: List Approvals

Retrieves pending approvals from a Nucleus One project.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-approvals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-approvals?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-approvals?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor. Leave empty to get the first page of results. Example: `Paste a cursor from a previous response`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AssetItemTags": [
        {}
      ],
      "AssignmentUserEmail": "ava@example.com",
      "AssignmentUserName": "Ava Chen",
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "DocumentCreatedByUserEmail": "ava@example.com",
      "DocumentCreatedByUserID": "string",
      "DocumentCreatedByUserName": "Ava Chen",
      "DocumentCreatedOn": "2026-05-07T12:00:00.000Z",
      "DocumentFileSize": 1,
      "DocumentIsSigned": true,
      "DocumentName": "Ava Chen",
      "DocumentPageCount": 1,
      "DocumentPreviewMetadata": [
        {}
      ],
      "ID": "string",
      "ItemAncestorIDs": [
        "string"
      ],
      "ItemCompletedByUserEmail": "ava@example.com",
      "ItemCompletedByUserID": "string",
      "ItemCompletedByUserName": "Ava Chen",
      "ItemCompletedOn": "2026-05-07T12:00:00.000Z",
      "ItemCreatedByUserEmail": "ava@example.com",
      "ItemCreatedByUserID": "string",
      "ItemCreatedByUserName": "Ava Chen",
      "ItemCreatedOn": "2026-05-07T12:00:00.000Z",
      "ItemDescription": "string",
      "ItemID": "string",
      "ItemName": "Ava Chen",
      "ItemParentName": "Ava Chen",
      "ItemPreviewMetadata": [
        {}
      ],
      "ItemType": "string",
      "OrganizationID": "string",
      "ProcessElementID": "string",
      "ProcessElementName": "Ava Chen",
      "ProcessID": "string",
      "ProcessName": "Ava Chen",
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "ReceivedFromEmail": "ava@example.com",
      "ReceivedFromName": "Ava Chen",
      "ReceivedFromResult": "string",
      "Result": "string",
      "Tags": [
        "string"
      ],
      "TaskDueOn": "2026-05-07T12:00:00.000Z",
      "ThumbnailUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AssetItemTags` | array<object> |  |
| `AssignmentUserEmail` | string |  |
| `AssignmentUserName` | string |  |
| `CreatedOn` | date |  |
| `DocumentCreatedByUserEmail` | string |  |
| `DocumentCreatedByUserID` | string |  |
| `DocumentCreatedByUserName` | string |  |
| `DocumentCreatedOn` | date |  |
| `DocumentFileSize` | number |  |
| `DocumentIsSigned` | boolean |  |
| `DocumentName` | string |  |
| `DocumentPageCount` | number |  |
| `DocumentPreviewMetadata` | array<object> |  |
| `ID` | string |  |
| `ItemAncestorIDs` | array<string> |  |
| `ItemCompletedByUserEmail` | string |  |
| `ItemCompletedByUserID` | string |  |
| `ItemCompletedByUserName` | string |  |
| `ItemCompletedOn` | date |  |
| `ItemCreatedByUserEmail` | string |  |
| `ItemCreatedByUserID` | string |  |
| `ItemCreatedByUserName` | string |  |
| `ItemCreatedOn` | date |  |
| `ItemDescription` | string |  |
| `ItemID` | string |  |
| `ItemName` | string |  |
| `ItemParentName` | string |  |
| `ItemPreviewMetadata` | array<object> |  |
| `ItemType` | string |  |
| `OrganizationID` | string |  |
| `ProcessElementID` | string |  |
| `ProcessElementName` | string |  |
| `ProcessID` | string |  |
| `ProcessName` | string |  |
| `ProjectID` | string |  |
| `ProjectName` | string |  |
| `ReceivedFromEmail` | string |  |
| `ReceivedFromName` | string |  |
| `ReceivedFromResult` | string |  |
| `Result` | string |  |
| `Tags` | array<string> |  |
| `TaskDueOn` | date |  |
| `ThumbnailUrl` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/approvals` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-approvals.md) for the provider-specific parameters and requirements.


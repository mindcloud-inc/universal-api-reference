# Nucleus One: Search Organization Content

Finds organization content in Nucleus One by search query.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/search-organization-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/search-organization-content?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/search-organization-content?${params}`, {
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
      "AncestorIDs": [
        "string"
      ],
      "Archived": true,
      "AssetID": "string",
      "AssetItemTags": [
        {}
      ],
      "AssetName": "Ava Chen",
      "AssetPluralName": "Ava Chen",
      "AssignmentUserEmail": "ava@example.com",
      "AssignmentUserEmails": [
        "ava@example.com"
      ],
      "AssignmentUserName": "Ava Chen",
      "CompletedByUserEmail": "ava@example.com",
      "CompletedByUserName": "Ava Chen",
      "CompletedOn": "2026-05-07T12:00:00.000Z",
      "ContentType": "string",
      "CreatedByUserEmail": "ava@example.com",
      "CreatedByUserName": "Ava Chen",
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "Description": "string",
      "DocumentFolderHexColor": "string",
      "DocumentFolderID": "string",
      "DocumentFolderPath": "string",
      "DocumentID": "string",
      "DocumentOrigin": "string",
      "DocumentSignatureSessionID": "string",
      "DocumentSignatureSessionIsActive": true,
      "DueOn": "2026-05-07T12:00:00.000Z",
      "FileSize": 1,
      "FormTemplateID": "string",
      "FormTemplateUniqueID": "string",
      "Highlights": [
        {}
      ],
      "ID": "string",
      "IsSigned": true,
      "ItemAncestorIDs": [
        "string"
      ],
      "ItemID": "string",
      "ItemType": "string",
      "Name": "Ava Chen",
      "OrganizationID": "string",
      "PageCount": 1,
      "PreviewMetadata": [
        {}
      ],
      "PrimaryDocument": {},
      "Priority": 1,
      "ProcessElementName": "Ava Chen",
      "ProcessName": "Ava Chen",
      "ProjectAccess": {},
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "PurgeDate": "2026-05-07T12:00:00.000Z",
      "Result": "string",
      "Score": 1,
      "Tags": [
        "string"
      ],
      "TaskDurationInterval": "string",
      "TaskDurationMultiplier": 1,
      "TaskMilestoneName": "Ava Chen",
      "TaskStateName": "Ava Chen",
      "ThumbnailUrl": "https://example.com",
      "UniqueID": "string",
      "UserEmail": "ava@example.com",
      "UserName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AncestorIDs` | array<string> |  |
| `Archived` | boolean |  |
| `AssetID` | string |  |
| `AssetItemTags` | array<object> |  |
| `AssetName` | string |  |
| `AssetPluralName` | string |  |
| `AssignmentUserEmail` | string |  |
| `AssignmentUserEmails` | array<string> |  |
| `AssignmentUserName` | string |  |
| `CompletedByUserEmail` | string |  |
| `CompletedByUserName` | string |  |
| `CompletedOn` | date |  |
| `ContentType` | string |  |
| `CreatedByUserEmail` | string |  |
| `CreatedByUserName` | string |  |
| `CreatedOn` | date |  |
| `Description` | string |  |
| `DocumentFolderHexColor` | string |  |
| `DocumentFolderID` | string |  |
| `DocumentFolderPath` | string |  |
| `DocumentID` | string |  |
| `DocumentOrigin` | string |  |
| `DocumentSignatureSessionID` | string |  |
| `DocumentSignatureSessionIsActive` | boolean |  |
| `DueOn` | date |  |
| `FileSize` | number |  |
| `FormTemplateID` | string |  |
| `FormTemplateUniqueID` | string |  |
| `Highlights` | array<object> |  |
| `ID` | string |  |
| `IsSigned` | boolean |  |
| `ItemAncestorIDs` | array<string> |  |
| `ItemID` | string |  |
| `ItemType` | string |  |
| `Name` | string |  |
| `OrganizationID` | string |  |
| `PageCount` | number |  |
| `PreviewMetadata` | array<object> |  |
| `PrimaryDocument` | object |  |
| `Priority` | number |  |
| `ProcessElementName` | string |  |
| `ProcessName` | string |  |
| `ProjectAccess` | object |  |
| `ProjectID` | string |  |
| `ProjectName` | string |  |
| `PurgeDate` | date |  |
| `Result` | string |  |
| `Score` | number |  |
| `Tags` | array<string> |  |
| `TaskDurationInterval` | string |  |
| `TaskDurationMultiplier` | number |  |
| `TaskMilestoneName` | string |  |
| `TaskStateName` | string |  |
| `ThumbnailUrl` | string |  |
| `UniqueID` | string |  |
| `UserEmail` | string |  |
| `UserName` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/searchResults` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-organization-content.md) for the provider-specific parameters and requirements.


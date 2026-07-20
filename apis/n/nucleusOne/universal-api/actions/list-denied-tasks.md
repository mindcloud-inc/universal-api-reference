# Nucleus One: List Denied Tasks

Retrieves denied tasks from a Nucleus One project.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-denied-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-denied-tasks?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-denied-tasks?${params}`, {
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
      "$schema": "string",
      "AssetItemTagAssetItemIDs": [
        "string"
      ],
      "AssetItemTags": [
        {}
      ],
      "AssignmentUserEmail": "ava@example.com",
      "AssignmentUserName": "Ava Chen",
      "AssignmentUserNameLower": "Ava Chen",
      "CompletedByUserEmail": "ava@example.com",
      "CompletedByUserID": "string",
      "CompletedByUserName": "Ava Chen",
      "CompletedOn": "2026-05-07T12:00:00.000Z",
      "CreatedByUserEmail": "ava@example.com",
      "CreatedByUserID": "string",
      "CreatedByUserName": "Ava Chen",
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "Description": "string",
      "DescriptionHtml": "string",
      "DescriptionRichTextJson": "string",
      "DueOn": "2026-05-07T12:00:00.000Z",
      "DueOnModifiedOn": "2026-05-07T12:00:00.000Z",
      "DurationInterval": "string",
      "DurationMultiplier": 1,
      "ID": "string",
      "ModifiedByUserEmail": "ava@example.com",
      "ModifiedByUserID": "string",
      "ModifiedByUserName": "Ava Chen",
      "ModifiedOn": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "NameLower": "Ava Chen",
      "OrganizationID": "string",
      "ParentTaskID": "string",
      "PrimaryDocument": {},
      "Priority": 1,
      "ProcessElementID": "string",
      "ProcessElementName": "Ava Chen",
      "ProcessElementNameLower": "Ava Chen",
      "ProcessID": "string",
      "ProcessName": "Ava Chen",
      "ProcessNameLower": "Ava Chen",
      "ProjectAccess": {},
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "Reminder_1_Day": "2026-05-07T12:00:00.000Z",
      "Reminder_3_Day": "2026-05-07T12:00:00.000Z",
      "Reminder_7_Day": "2026-05-07T12:00:00.000Z",
      "Result": "string",
      "Revision": 1,
      "Stakeholders": [
        {}
      ],
      "SubTasks": [
        {}
      ],
      "Tags": [
        "string"
      ],
      "TaskMilestoneID": "string",
      "TaskMilestoneName": "Ava Chen",
      "TaskMilestoneNameLower": "Ava Chen",
      "TaskStateID": "string",
      "TaskStateName": "Ava Chen",
      "TaskStateNameLower": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `AssetItemTagAssetItemIDs` | array<string> |  |
| `AssetItemTags` | array<object> |  |
| `AssignmentUserEmail` | string |  |
| `AssignmentUserName` | string |  |
| `AssignmentUserNameLower` | string |  |
| `CompletedByUserEmail` | string |  |
| `CompletedByUserID` | string |  |
| `CompletedByUserName` | string |  |
| `CompletedOn` | date |  |
| `CreatedByUserEmail` | string |  |
| `CreatedByUserID` | string |  |
| `CreatedByUserName` | string |  |
| `CreatedOn` | date |  |
| `Description` | string |  |
| `DescriptionHtml` | string |  |
| `DescriptionRichTextJson` | string |  |
| `DueOn` | date |  |
| `DueOnModifiedOn` | date |  |
| `DurationInterval` | string |  |
| `DurationMultiplier` | number |  |
| `ID` | string |  |
| `ModifiedByUserEmail` | string |  |
| `ModifiedByUserID` | string |  |
| `ModifiedByUserName` | string |  |
| `ModifiedOn` | date |  |
| `Name` | string |  |
| `NameLower` | string |  |
| `OrganizationID` | string |  |
| `ParentTaskID` | string |  |
| `PrimaryDocument` | object |  |
| `Priority` | number |  |
| `ProcessElementID` | string |  |
| `ProcessElementName` | string |  |
| `ProcessElementNameLower` | string |  |
| `ProcessID` | string |  |
| `ProcessName` | string |  |
| `ProcessNameLower` | string |  |
| `ProjectAccess` | object |  |
| `ProjectID` | string |  |
| `ProjectName` | string |  |
| `Reminder_1_Day` | date |  |
| `Reminder_3_Day` | date |  |
| `Reminder_7_Day` | date |  |
| `Result` | string |  |
| `Revision` | number |  |
| `Stakeholders` | array<object> |  |
| `SubTasks` | array<object> |  |
| `Tags` | array<string> |  |
| `TaskMilestoneID` | string |  |
| `TaskMilestoneName` | string |  |
| `TaskMilestoneNameLower` | string |  |
| `TaskStateID` | string |  |
| `TaskStateName` | string |  |
| `TaskStateNameLower` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/deniedTasks` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-denied-tasks.md) for the provider-specific parameters and requirements.


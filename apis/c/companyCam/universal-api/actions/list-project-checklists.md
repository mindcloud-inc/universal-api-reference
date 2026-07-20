# CompanyCam: List Project Checklists

Retrieve all checklists for a CompanyCam project.

```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-project-checklists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-project-checklists?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-project-checklists?${params}`, {
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
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checklistTemplateId": 1,
      "companyId": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "id": "string",
      "isPopulating": true,
      "name": "Ava Chen",
      "projectId": "string",
      "sections": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "creatorId": "string",
          "creatorName": "Ava Chen",
          "creatorType": "string",
          "id": "string",
          "position": 1,
          "tasks": [
            {
              "completedAt": "2026-05-07T12:00:00.000Z",
              "completedById": "string",
              "completedByType": "string",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "creatorId": "string",
              "creatorType": "string",
              "details": "string",
              "id": "string",
              "photoCaptureRequired": true,
              "position": 1,
              "subTasks": [
                {
                  "answerChoices": [
                    1
                  ],
                  "answerOptions": [
                    "string"
                  ],
                  "answerText": {},
                  "answerType": "string",
                  "id": "string",
                  "label": "string",
                  "position": 1,
                  "taskId": 1
                }
              ],
              "title": "string",
              "todoListId": "string",
              "todoListSectionId": "string",
              "updatedAt": "2026-05-07T12:00:00.000Z"
            }
          ],
          "title": "string",
          "todoListId": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checklistTemplateId` | number |  |
| `companyId` | string |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `id` | string |  |
| `isPopulating` | boolean |  |
| `name` | string |  |
| `projectId` | string |  |
| `sections[].createdAt` | date |  |
| `sections[].creatorId` | string |  |
| `sections[].creatorName` | string |  |
| `sections[].creatorType` | string |  |
| `sections[].id` | string |  |
| `sections[].position` | number |  |
| `sections[].tasks[].completedAt` | date |  |
| `sections[].tasks[].completedById` | string |  |
| `sections[].tasks[].completedByType` | string |  |
| `sections[].tasks[].createdAt` | date |  |
| `sections[].tasks[].creatorId` | string |  |
| `sections[].tasks[].creatorType` | string |  |
| `sections[].tasks[].details` | string |  |
| `sections[].tasks[].id` | string |  |
| `sections[].tasks[].photoCaptureRequired` | boolean |  |
| `sections[].tasks[].position` | number |  |
| `sections[].tasks[].subTasks[].answerChoices[]` | number |  |
| `sections[].tasks[].subTasks[].answerOptions[]` | string |  |
| `sections[].tasks[].subTasks[].answerText` | object |  |
| `sections[].tasks[].subTasks[].answerType` | string |  |
| `sections[].tasks[].subTasks[].id` | string |  |
| `sections[].tasks[].subTasks[].label` | string |  |
| `sections[].tasks[].subTasks[].position` | number |  |
| `sections[].tasks[].subTasks[].taskId` | number |  |
| `sections[].tasks[].title` | string |  |
| `sections[].tasks[].todoListId` | string |  |
| `sections[].tasks[].todoListSectionId` | string |  |
| `sections[].tasks[].updatedAt` | date |  |
| `sections[].title` | string |  |
| `sections[].todoListId` | string |  |
| `sections[].updatedAt` | date |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET projects/:projectId/checklists` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-checklists.md) for the provider-specific parameters and requirements.


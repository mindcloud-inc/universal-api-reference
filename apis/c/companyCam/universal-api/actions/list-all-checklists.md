# CompanyCam: List All Checklists

Retrieves a list of checklists from CompanyCam.

```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-all-checklists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-all-checklists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-all-checklists?${params}`, {
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
| `completed` | boolean | no |  |
| `updatedSince` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checklistTemplateId": 1,
      "companyId": "string",
      "completedAt": 1,
      "createdAt": 1,
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "id": "string",
      "isPopulating": true,
      "name": "Ava Chen",
      "projectId": "string",
      "sections": [
        {
          "createdAt": 1,
          "creatorId": "string",
          "creatorName": "Ava Chen",
          "creatorType": "string",
          "id": "string",
          "position": 1,
          "tasks": [
            {
              "completedAt": 1,
              "completedById": "string",
              "completedByType": "string",
              "createdAt": 1,
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
              "updatedAt": 1
            }
          ],
          "title": "string",
          "todoListId": "string",
          "updatedAt": 1
        }
      ],
      "updatedAt": 1
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
| `completedAt` | number |  |
| `createdAt` | number |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `id` | string |  |
| `isPopulating` | boolean |  |
| `name` | string |  |
| `projectId` | string |  |
| `sections[].createdAt` | number |  |
| `sections[].creatorId` | string |  |
| `sections[].creatorName` | string |  |
| `sections[].creatorType` | string |  |
| `sections[].id` | string |  |
| `sections[].position` | number |  |
| `sections[].tasks[].completedAt` | number |  |
| `sections[].tasks[].completedById` | string |  |
| `sections[].tasks[].completedByType` | string |  |
| `sections[].tasks[].createdAt` | number |  |
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
| `sections[].tasks[].updatedAt` | number |  |
| `sections[].title` | string |  |
| `sections[].todoListId` | string |  |
| `sections[].updatedAt` | number |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET checklists` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-checklists.md) for the provider-specific parameters and requirements.


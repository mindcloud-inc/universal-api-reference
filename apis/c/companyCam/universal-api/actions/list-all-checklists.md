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

## Response

```json
{
  "success": true,
  "data": [
    {
      "checklistTemplateId": {},
      "companyId": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "id": "string",
      "isPopulating": {},
      "name": "Ava Chen",
      "projectId": "string",
      "sectionlessTasks": [
        {
          "completedAt": "2026-05-07T12:00:00.000Z",
          "completedById": "string",
          "completedByType": {},
          "createdAt": "2026-05-07T12:00:00.000Z",
          "creatorId": "string",
          "creatorType": "string",
          "details": "string",
          "id": "string",
          "photoCaptureRequired": true,
          "position": 1,
          "title": "string",
          "todoListId": "string",
          "todoListSectionId": "string",
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
| `checklistTemplateId` | object |  |
| `companyId` | string |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `id` | string |  |
| `isPopulating` | object |  |
| `name` | string |  |
| `projectId` | string |  |
| `sectionlessTasks[].completedAt` | date |  |
| `sectionlessTasks[].completedById` | string |  |
| `sectionlessTasks[].completedByType` | object |  |
| `sectionlessTasks[].createdAt` | date |  |
| `sectionlessTasks[].creatorId` | string |  |
| `sectionlessTasks[].creatorType` | string |  |
| `sectionlessTasks[].details` | string |  |
| `sectionlessTasks[].id` | string |  |
| `sectionlessTasks[].photoCaptureRequired` | boolean |  |
| `sectionlessTasks[].position` | number |  |
| `sectionlessTasks[].title` | string |  |
| `sectionlessTasks[].todoListId` | string |  |
| `sectionlessTasks[].todoListSectionId` | string |  |
| `sectionlessTasks[].updatedAt` | date |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET checklists` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-checklists.md) for the provider-specific parameters and requirements.


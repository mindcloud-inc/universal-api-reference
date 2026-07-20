# Crowdin: List Project Tasks

Retrieves project tasks from Crowdin.

```
GET https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-project-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-project-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-project-tasks?${params}`, {
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
| `projectId` | number | yes |  |
| `orderBy` | string | no |  |
| `status` | string | no |  |
| `assigneeId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualCost": 1,
      "assignedTeams": [
        {}
      ],
      "assignees": [
        {}
      ],
      "batchId": 1,
      "buyUrl": "https://example.com",
      "commentsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": 1,
      "deadline": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "estimatedCost": 1,
      "excludeLabelIds": [
        1
      ],
      "excludeLabelMatchRule": "string",
      "fileIds": [
        1
      ],
      "filesCount": 1,
      "generateCostEstimate": true,
      "generateTranslationCost": true,
      "id": 1,
      "labelIds": [
        1
      ],
      "labelMatchRule": "string",
      "precedingTaskId": 1,
      "progress": {},
      "projectId": 1,
      "reportSettingsTemplateId": 1,
      "resolvedAt": "2026-05-07T12:00:00.000Z",
      "sourceLanguage": {},
      "sourceLanguageId": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "targetLanguageId": "string",
      "targetLanguages": [
        {}
      ],
      "timeRange": {},
      "title": "string",
      "translateProgress": 1,
      "translationsUpdatedTimeRange": {},
      "translationUrl": "https://example.com",
      "type": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vendor": "string",
      "webUrl": "https://example.com",
      "wordsCount": 1,
      "workflowStepId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualCost` | number |  |
| `assignedTeams` | array<object> |  |
| `assignees` | array<object> |  |
| `batchId` | number |  |
| `buyUrl` | string |  |
| `commentsCount` | number |  |
| `createdAt` | date |  |
| `creatorId` | number |  |
| `deadline` | date |  |
| `description` | string |  |
| `estimatedCost` | number |  |
| `excludeLabelIds` | array<number> |  |
| `excludeLabelMatchRule` | string |  |
| `fileIds` | array<number> |  |
| `filesCount` | number |  |
| `generateCostEstimate` | boolean |  |
| `generateTranslationCost` | boolean |  |
| `id` | number |  |
| `labelIds` | array<number> |  |
| `labelMatchRule` | string |  |
| `precedingTaskId` | number |  |
| `progress` | object |  |
| `projectId` | number |  |
| `reportSettingsTemplateId` | number |  |
| `resolvedAt` | date |  |
| `sourceLanguage` | object |  |
| `sourceLanguageId` | string |  |
| `startedAt` | date |  |
| `status` | string |  |
| `targetLanguageId` | string |  |
| `targetLanguages` | array<object> |  |
| `timeRange` | object |  |
| `title` | string |  |
| `translateProgress` | number |  |
| `translationsUpdatedTimeRange` | object |  |
| `translationUrl` | string |  |
| `type` | number |  |
| `updatedAt` | date |  |
| `vendor` | string |  |
| `webUrl` | string |  |
| `wordsCount` | number |  |
| `workflowStepId` | number |  |

## Native endpoint

Through the native Crowdin API, this operation is `GET /projects/:projectId/tasks` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-tasks.md) for the provider-specific parameters and requirements.


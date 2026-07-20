# Galileo: Get Project

Retrieves a project from Galileo by ID.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | Galileo project UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookmark": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByUser": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen"
      },
      "description": "string",
      "id": "string",
      "labels": [
        "string"
      ],
      "name": "Ava Chen",
      "permissions": [
        {
          "action": "string",
          "allowed": true,
          "message": "string"
        }
      ],
      "runs": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": "string",
          "creator": {},
          "datasetHash": "string",
          "datasetVersionId": "string",
          "exampleContentId": "string",
          "id": "string",
          "lastUpdatedBy": "string",
          "loggedInferenceNames": [
            "Ava Chen"
          ],
          "loggedSplits": [
            "string"
          ],
          "name": "Ava Chen",
          "numSamples": 1,
          "projectId": "string",
          "runTags": [
            {
              "createdAt": "2026-05-07T12:00:00.000Z",
              "createdBy": "string",
              "id": "string",
              "key": "string",
              "projectId": "string",
              "runId": "string",
              "tagType": "string",
              "updatedAt": "2026-05-07T12:00:00.000Z",
              "value": "string"
            }
          ],
          "taskType": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "winner": true
        }
      ],
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookmark` | boolean |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByUser.email` | string |  |
| `createdByUser.firstName` | string |  |
| `createdByUser.id` | string |  |
| `createdByUser.lastName` | string |  |
| `description` | string |  |
| `id` | string |  |
| `labels` | array<string> |  |
| `name` | string |  |
| `permissions` | array<object> |  |
| `permissions[].action` | string |  |
| `permissions[].allowed` | boolean |  |
| `permissions[].message` | string |  |
| `runs` | array<object> |  |
| `runs[].createdAt` | date |  |
| `runs[].createdBy` | string |  |
| `runs[].creator` | object |  |
| `runs[].datasetHash` | string |  |
| `runs[].datasetVersionId` | string |  |
| `runs[].exampleContentId` | string |  |
| `runs[].id` | string |  |
| `runs[].lastUpdatedBy` | string |  |
| `runs[].loggedInferenceNames` | array<string> |  |
| `runs[].loggedSplits` | array<string> |  |
| `runs[].name` | string |  |
| `runs[].numSamples` | number |  |
| `runs[].projectId` | string |  |
| `runs[].runTags` | array<object> |  |
| `runs[].runTags[].createdAt` | date |  |
| `runs[].runTags[].createdBy` | string |  |
| `runs[].runTags[].id` | string |  |
| `runs[].runTags[].key` | string |  |
| `runs[].runTags[].projectId` | string |  |
| `runs[].runTags[].runId` | string |  |
| `runs[].runTags[].tagType` | string |  |
| `runs[].runTags[].updatedAt` | date |  |
| `runs[].runTags[].value` | string |  |
| `runs[].taskType` | number |  |
| `runs[].updatedAt` | date |  |
| `runs[].winner` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/projects/:project_id` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.


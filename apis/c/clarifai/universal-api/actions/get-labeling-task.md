# Clarifai: Get Labeling Task

Retrieves a labeling task from Clarifai.

```
GET https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/get-labeling-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/get-labeling-task?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/get-labeling-task?${params}`, {
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
| `appId` | string | no |  |
| `taskId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": {
        "code": 1,
        "description": "string",
        "httpStatusCode": 1,
        "reqId": "string"
      },
      "task": {
        "appId": "string",
        "conceptIds": [
          "string"
        ],
        "concepts": [
          {
            "concept": {
              "appId": "string",
              "id": "string",
              "name": "Ava Chen",
              "userId": "string",
              "value": 1
            }
          }
        ],
        "createdAt": "string",
        "id": "string",
        "inputSource": {
          "id": "string",
          "type": 1
        },
        "modifiedAt": "string",
        "name": "Ava Chen",
        "priority": 1,
        "review": {
          "strategy": 1
        },
        "status": {
          "code": 1
        },
        "type": 1,
        "userId": "string",
        "visibility": {
          "gettable": 1
        },
        "worker": {
          "strategy": 1,
          "type": 1,
          "userIds": [
            "string"
          ],
          "users": [
            {
              "id": "string"
            }
          ],
          "workers": [
            {
              "user": {
                "id": "string"
              }
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.httpStatusCode` | number |  |
| `status.reqId` | string |  |
| `task.appId` | string |  |
| `task.conceptIds[]` | string |  |
| `task.concepts[].concept.appId` | string |  |
| `task.concepts[].concept.id` | string |  |
| `task.concepts[].concept.name` | string |  |
| `task.concepts[].concept.userId` | string |  |
| `task.concepts[].concept.value` | number |  |
| `task.createdAt` | string |  |
| `task.id` | string |  |
| `task.inputSource.id` | string |  |
| `task.inputSource.type` | number |  |
| `task.modifiedAt` | string |  |
| `task.name` | string |  |
| `task.priority` | number |  |
| `task.review.strategy` | number |  |
| `task.status.code` | number |  |
| `task.type` | number |  |
| `task.userId` | string |  |
| `task.visibility.gettable` | number |  |
| `task.worker.strategy` | number |  |
| `task.worker.type` | number |  |
| `task.worker.userIds[]` | string |  |
| `task.worker.users[].id` | string |  |
| `task.worker.workers[].user.id` | string |  |

## Native endpoint

Through the native Clarifai API, this operation is `GET /v2/users/{{credentials.userId}}/apps/{{appId}}/tasks/{{taskId}}` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-labeling-task.md) for the provider-specific parameters and requirements.


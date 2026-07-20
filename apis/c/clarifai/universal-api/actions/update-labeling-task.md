# Clarifai: Update Labeling Task

Updates an existing labeling task in Clarifai.

```
PATCH https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-labeling-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PATCH "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-labeling-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-labeling-task', {
  method: 'PATCH',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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
      "tasks": [
        {
          "appId": "string",
          "conceptIds": [
            "string"
          ],
          "concepts": [
            {
              "concept": {
                "appId": "string",
                "id": "string",
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
      ]
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
| `tasks[].appId` | string |  |
| `tasks[].conceptIds[]` | string |  |
| `tasks[].concepts[].concept.appId` | string |  |
| `tasks[].concepts[].concept.id` | string |  |
| `tasks[].concepts[].concept.userId` | string |  |
| `tasks[].concepts[].concept.value` | number |  |
| `tasks[].createdAt` | string |  |
| `tasks[].id` | string |  |
| `tasks[].inputSource.id` | string |  |
| `tasks[].inputSource.type` | number |  |
| `tasks[].modifiedAt` | string |  |
| `tasks[].name` | string |  |
| `tasks[].priority` | number |  |
| `tasks[].review.strategy` | number |  |
| `tasks[].status.code` | number |  |
| `tasks[].type` | number |  |
| `tasks[].userId` | string |  |
| `tasks[].visibility.gettable` | number |  |
| `tasks[].worker.strategy` | number |  |
| `tasks[].worker.type` | number |  |
| `tasks[].worker.userIds[]` | string |  |
| `tasks[].worker.users[].id` | string |  |
| `tasks[].worker.workers[].user.id` | string |  |

## Native endpoint

Through the native Clarifai API, this operation is `PATCH /v2/tasks` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-labeling-task.md) for the provider-specific parameters and requirements.


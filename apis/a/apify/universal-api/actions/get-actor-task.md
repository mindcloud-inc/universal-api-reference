# Apify: Get Actor Task

Retrieves an actor task from Apify.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor-task?connectionId=$CONNECTION_ID&actorTaskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actorTaskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor-task?${params}`, {
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
| `actorTaskId` | string | yes | The ID of the actor task to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "actId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "input": {
          "message": "string"
        },
        "modifiedAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "options": {},
        "standbyUrl": {},
        "stats": {
          "lastRunStartedAt": "2026-05-07T12:00:00.000Z",
          "totalRuns": 1
        },
        "title": "string",
        "userId": "string",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.actId` | string |  |
| `data.createdAt` | date |  |
| `data.id` | string |  |
| `data.input.message` | string |  |
| `data.modifiedAt` | date |  |
| `data.name` | string |  |
| `data.options` | object |  |
| `data.standbyUrl` | object |  |
| `data.stats.lastRunStartedAt` | date |  |
| `data.stats.totalRuns` | number |  |
| `data.title` | string |  |
| `data.userId` | string |  |
| `data.username` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/actor-tasks/:actorTaskId` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-actor-task.md) for the provider-specific parameters and requirements.


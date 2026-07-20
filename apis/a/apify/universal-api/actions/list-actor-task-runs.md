# Apify: List Actor Task Runs

Retrieves runs for an Apify actor task.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/list-actor-task-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/list-actor-task-runs?connectionId=$CONNECTION_ID&actorTaskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actorTaskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/list-actor-task-runs?${params}`, {
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
| `actorTaskId` | string | yes | The ID of the actor task whose runs to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actId": "string",
      "actorTaskId": "string",
      "buildId": "string",
      "buildNumber": "string",
      "buildNumberInt": 1,
      "defaultDatasetId": "string",
      "defaultKeyValueStoreId": "string",
      "defaultRequestQueueId": "string",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "meta": {
        "origin": "string"
      },
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "usageTotalUsd": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actId` | string |  |
| `actorTaskId` | string |  |
| `buildId` | string |  |
| `buildNumber` | string |  |
| `buildNumberInt` | number |  |
| `defaultDatasetId` | string |  |
| `defaultKeyValueStoreId` | string |  |
| `defaultRequestQueueId` | string |  |
| `finishedAt` | date |  |
| `id` | string |  |
| `meta.origin` | string |  |
| `startedAt` | date |  |
| `status` | string |  |
| `usageTotalUsd` | number |  |
| `userId` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/actor-tasks/:actorTaskId/runs` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-actor-task-runs.md) for the provider-specific parameters and requirements.


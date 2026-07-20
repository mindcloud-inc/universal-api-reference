# Apify: Get Actor Run

Retrieves an actor run from Apify.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor-run?connectionId=$CONNECTION_ID&actorId=string&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actorId": "string",
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor-run?${params}`, {
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
| `actorId` | string | yes | The ID or username of the actor that owns the run. |
| `runId` | string | yes | The ID of the actor run to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "actId": "string",
        "actorTaskId": "string",
        "buildId": "string",
        "buildNumber": "string",
        "consoleUrl": "https://example.com",
        "defaultDatasetId": "string",
        "defaultKeyValueStoreId": "string",
        "defaultRequestQueueId": "string",
        "finishedAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "meta": {
          "origin": "string",
          "userAgent": "string"
        },
        "startedAt": "2026-05-07T12:00:00.000Z",
        "stats": {
          "computeUnits": 1,
          "durationMillis": 1,
          "runTimeSecs": 1
        },
        "status": "string",
        "usageTotalUsd": 1,
        "userId": "string"
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
| `data.actorTaskId` | string |  |
| `data.buildId` | string |  |
| `data.buildNumber` | string |  |
| `data.consoleUrl` | string |  |
| `data.defaultDatasetId` | string |  |
| `data.defaultKeyValueStoreId` | string |  |
| `data.defaultRequestQueueId` | string |  |
| `data.finishedAt` | date |  |
| `data.id` | string |  |
| `data.meta.origin` | string |  |
| `data.meta.userAgent` | string |  |
| `data.startedAt` | date |  |
| `data.stats.computeUnits` | number |  |
| `data.stats.durationMillis` | number |  |
| `data.stats.runTimeSecs` | number |  |
| `data.status` | string |  |
| `data.usageTotalUsd` | number |  |
| `data.userId` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/acts/:actorId/runs/:runId` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-actor-run.md) for the provider-specific parameters and requirements.


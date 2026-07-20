# Apify: Get Request Queue

Retrieves a request queue from Apify.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-request-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-request-queue?connectionId=$CONNECTION_ID&queueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-request-queue?${params}`, {
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
| `queueId` | string | yes | The ID of the request queue to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accessedAt": "2026-05-07T12:00:00.000Z",
        "actId": {},
        "actRunId": {},
        "consoleUrl": "https://example.com",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "generalAccess": "string",
        "hadMultipleClients": true,
        "handledRequestCount": 1,
        "id": "string",
        "modifiedAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "pendingRequestCount": 1,
        "stats": {
          "deleteCount": 1,
          "headItemReadCount": 1,
          "readCount": 1,
          "storageBytes": 1,
          "writeCount": 1
        },
        "totalRequestCount": 1,
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
| `data.accessedAt` | date |  |
| `data.actId` | object |  |
| `data.actRunId` | object |  |
| `data.consoleUrl` | string |  |
| `data.createdAt` | date |  |
| `data.generalAccess` | string |  |
| `data.hadMultipleClients` | boolean |  |
| `data.handledRequestCount` | number |  |
| `data.id` | string |  |
| `data.modifiedAt` | date |  |
| `data.name` | string |  |
| `data.pendingRequestCount` | number |  |
| `data.stats.deleteCount` | number |  |
| `data.stats.headItemReadCount` | number |  |
| `data.stats.readCount` | number |  |
| `data.stats.storageBytes` | number |  |
| `data.stats.writeCount` | number |  |
| `data.totalRequestCount` | number |  |
| `data.userId` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/request-queues/:queueId` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-request-queue.md) for the provider-specific parameters and requirements.


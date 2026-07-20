# CloudConvert: Create Import URL Task

Creates an import-by-URL task in CloudConvert.

```
POST https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/create-import-url-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/create-import-url-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/create-import-url-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Source URL to import from. |
| `filename` | string | no | Optional filename to assign to the imported file. |
| `headers` | object | no | Optional HTTP headers to send when fetching the source URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "copyOfTaskId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "credits": "string",
      "endedAt": "string",
      "hostName": "Ava Chen",
      "id": "string",
      "jobId": "string",
      "links": {
        "self": "https://example.com"
      },
      "message": "string",
      "operation": "string",
      "percent": 1,
      "priority": 1,
      "region": "string",
      "result": "string",
      "retryOfTaskId": "string",
      "startedAt": "string",
      "status": "string",
      "storage": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `copyOfTaskId` | string |  |
| `createdAt` | date |  |
| `credits` | string |  |
| `endedAt` | string |  |
| `hostName` | string |  |
| `id` | string |  |
| `jobId` | string |  |
| `links.self` | string |  |
| `message` | string |  |
| `operation` | string |  |
| `percent` | number |  |
| `priority` | number |  |
| `region` | string |  |
| `result` | string |  |
| `retryOfTaskId` | string |  |
| `startedAt` | string |  |
| `status` | string |  |
| `storage` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native CloudConvert API, this operation is `POST /import/url` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-import-url-task.md) for the provider-specific parameters and requirements.


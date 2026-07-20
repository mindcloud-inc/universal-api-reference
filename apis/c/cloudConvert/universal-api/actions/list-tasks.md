# CloudConvert: List Tasks

Retrieves tasks from your CloudConvert account.

```
GET https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "name": "Ava Chen",
      "operation": "string",
      "percent": 1,
      "priority": 1,
      "region": "string",
      "result": {
        "form": {
          "parameters": {
            "acl": "string",
            "key": "string",
            "policy": "string",
            "successActionRedirect": "string",
            "successActionStatus": "string",
            "xAmzAlgorithm": "string",
            "xAmzCredential": "string",
            "xAmzDate": "string",
            "xAmzSignature": "string"
          },
          "url": "https://example.com"
        }
      },
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
| `name` | string |  |
| `operation` | string |  |
| `percent` | number |  |
| `priority` | number |  |
| `region` | string |  |
| `result.form.parameters.acl` | string |  |
| `result.form.parameters.key` | string |  |
| `result.form.parameters.policy` | string |  |
| `result.form.parameters.successActionRedirect` | string |  |
| `result.form.parameters.successActionStatus` | string |  |
| `result.form.parameters.xAmzAlgorithm` | string |  |
| `result.form.parameters.xAmzCredential` | string |  |
| `result.form.parameters.xAmzDate` | string |  |
| `result.form.parameters.xAmzSignature` | string |  |
| `result.form.url` | string |  |
| `retryOfTaskId` | string |  |
| `startedAt` | string |  |
| `status` | string |  |
| `storage` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native CloudConvert API, this operation is `GET /tasks` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.


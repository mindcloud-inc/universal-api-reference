# mails.so: Retrieve Batch Validation Job

Retrieves a batch validation job from mails.so.

```
GET https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/retrieve-batch-validation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mails.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/retrieve-batch-validation-job?connectionId=$CONNECTION_ID&id=45a4cc93-0901-407a-8469-bc4ebb85503d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "45a4cc93-0901-407a-8469-bc4ebb85503d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/retrieve-batch-validation-job?${params}`, {
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
| `id` | string | yes | Batch validation job ID Example: `45a4cc93-0901-407a-8469-bc4ebb85503d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "duration": 1,
      "emails": [
        {
          "avatar": "ava@example.com",
          "didYouMean": "ava@example.com",
          "domain": "ava@example.com",
          "email": "ava@example.com",
          "id": "ava@example.com",
          "isDisposable": true,
          "isFree": true,
          "isvDomain": true,
          "isvFormat": true,
          "isvMx": true,
          "isvNoblock": true,
          "isvNocatchall": true,
          "isvNogeneric": true,
          "mxRecord": "ava@example.com",
          "provider": "ava@example.com",
          "reason": "ava@example.com",
          "result": "ava@example.com",
          "score": 1,
          "username": "ava@example.com"
        }
      ],
      "finishedAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "progress": 1,
      "size": 1,
      "stats": {
        "deliverable": 1,
        "noConnect": 1,
        "risky": 1,
        "total": 1,
        "undeliverable": 1,
        "unknown": 1
      },
      "status": "string",
      "type": "string",
      "updatedAt": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `duration` | number |  |
| `emails` | array<object> |  |
| `emails[].avatar` | string |  |
| `emails[].didYouMean` | string |  |
| `emails[].domain` | string |  |
| `emails[].email` | string |  |
| `emails[].id` | string |  |
| `emails[].isDisposable` | boolean |  |
| `emails[].isFree` | boolean |  |
| `emails[].isvDomain` | boolean |  |
| `emails[].isvFormat` | boolean |  |
| `emails[].isvMx` | boolean |  |
| `emails[].isvNoblock` | boolean |  |
| `emails[].isvNocatchall` | boolean |  |
| `emails[].isvNogeneric` | boolean |  |
| `emails[].mxRecord` | string |  |
| `emails[].provider` | string |  |
| `emails[].reason` | string |  |
| `emails[].result` | string |  |
| `emails[].score` | number |  |
| `emails[].username` | string |  |
| `finishedAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `progress` | number |  |
| `size` | number |  |
| `stats` | object |  |
| `stats.deliverable` | number |  |
| `stats.noConnect` | number |  |
| `stats.risky` | number |  |
| `stats.total` | number |  |
| `stats.undeliverable` | number |  |
| `stats.unknown` | number |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native mails.so API, this operation is `GET /batch/:id` (base URL `https://api.mails.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-batch-validation-job.md) for the provider-specific parameters and requirements.


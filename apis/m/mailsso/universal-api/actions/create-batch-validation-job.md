# mails.so: Create Batch Validation Job

Creates a new batch validation job in mails.so.

```
POST https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/create-batch-validation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mails.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/create-batch-validation-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": "user@example.com,hello@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/create-batch-validation-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": "user@example.com,hello@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes | Email addresses to validate in this batch Example: `user@example.com,hello@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "duration": 1,
      "finishedAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "progress": 1,
      "size": 1,
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
| `finishedAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `progress` | number |  |
| `size` | number |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native mails.so API, this operation is `POST /batch` (base URL `https://api.mails.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch-validation-job.md) for the provider-specific parameters and requirements.


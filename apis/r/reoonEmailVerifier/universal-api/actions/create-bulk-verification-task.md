# Reoon Email Verifier: Create Bulk Verification Task



```
POST https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/create-bulk-verification-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reoon Email Verifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/create-bulk-verification-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/create-bulk-verification-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Optional task name shown in Reoon. Example: `Newsletter cleanup`. |
| `emails` | object<string> | yes | Array of email addresses to verify in bulk. Serialized as a JSON array for Reoon bulk task creation. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count_duplicates_removed": 1,
      "count_processing": 1,
      "count_rejected_emails": 1,
      "count_submitted": 1,
      "status": "string",
      "task_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count_duplicates_removed` | number |  |
| `count_processing` | number |  |
| `count_rejected_emails` | number |  |
| `count_submitted` | number |  |
| `status` | string |  |
| `task_id` | number |  |

## Native endpoint

Through the native Reoon Email Verifier API, this operation is `POST /create-bulk-verification-task/` (base URL `https://emailverifier.reoon.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-verification-task.md) for the provider-specific parameters and requirements.


# TaskForce: Create Dispute

Creates a dispute for a rejected submission in TaskForce.

```
POST https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/create-dispute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaskForce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/create-dispute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reason": "string",
  "submissionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/create-dispute', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reason": "string",
    "submissionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reason` | string | yes | Why the rejection was unfair. |
| `submissionId` | string | yes | Rejected submission identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dispute": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dispute` | object | Created dispute payload. |

## Native endpoint

Through the native TaskForce API, this operation is `POST /disputes` (base URL `https://www.task-force.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dispute.md) for the provider-specific parameters and requirements.


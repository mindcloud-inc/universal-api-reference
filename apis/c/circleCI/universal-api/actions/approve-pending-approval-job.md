# CircleCI: Approve Pending Approval Job



```
PUT https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/approve-pending-approval-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/approve-pending-approval-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/approve-pending-approval-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `approval_request_id` | string | no | Approval request identifier. |
| `id` | string | no | Opaque workflow identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `POST /workflow/:id/approve/:approval_request_id` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-pending-approval-job.md) for the provider-specific parameters and requirements.


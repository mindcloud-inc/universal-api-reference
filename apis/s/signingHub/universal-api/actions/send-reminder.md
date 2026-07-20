# SigningHub: Send Reminder

Sends a workflow reminder in SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/send-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/send-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "order": "1",
  "packageId": "11191524"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/send-reminder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "order": "1",
    "packageId": "11191524"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | number | yes | Workflow order to remind. Example: `1`. |
| `packageId` | number | yes | Package ID of the workflow package. Example: `11191524`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SigningHub API returns.

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/:packageId/workflow/:order/remind` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-reminder.md) for the provider-specific parameters and requirements.


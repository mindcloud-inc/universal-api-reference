# Google Cloud Pub/Sub: Modify Ack Deadline

Modifies a subscription ack deadline in Google Cloud Pub/Sub.

```
PUT https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/modify-ack-deadline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/modify-ack-deadline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscription": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/modify-ack-deadline', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscription": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscription` | string | yes | Required. The name of the subscription. Format is `projects/{project}/subscriptions/{sub}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Pub/Sub API returns.

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `POST /v1/:subscription:modifyAckDeadline` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-ack-deadline.md) for the provider-specific parameters and requirements.


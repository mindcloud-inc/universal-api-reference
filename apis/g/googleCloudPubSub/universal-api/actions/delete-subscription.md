# Google Cloud Pub/Sub: Delete Subscription

Deletes a subscription from Google Cloud Pub/Sub.

```
DELETE https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/delete-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/delete-subscription?connectionId=$CONNECTION_ID&subscription=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscription": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/delete-subscription?${params}`, {
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
| `subscription` | string | yes | Required. The subscription to delete. Format is `projects/{project}/subscriptions/{sub}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Pub/Sub API returns.

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `DELETE /v1/:subscription` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscription.md) for the provider-specific parameters and requirements.


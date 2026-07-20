# Google Cloud Pub/Sub: Pull Messages

Pulls messages from Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/pull-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/pull-messages?connectionId=$CONNECTION_ID&subscription=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscription": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/pull-messages?${params}`, {
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
| `subscription` | string | yes | Required. The subscription from which messages should be pulled. Format is `projects/{project}/subscriptions/{sub}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "receivedMessages": [
        {
          "ackId": "string",
          "deliveryAttempt": 1,
          "message": {
            "data": "string",
            "messageId": "string",
            "orderingKey": "string",
            "publishTime": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `receivedMessages[].ackId` | string |  |
| `receivedMessages[].deliveryAttempt` | number |  |
| `receivedMessages[].message.data` | string |  |
| `receivedMessages[].message.messageId` | string |  |
| `receivedMessages[].message.orderingKey` | string |  |
| `receivedMessages[].message.publishTime` | string |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `POST /v1/:subscription:pull` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pull-messages.md) for the provider-specific parameters and requirements.


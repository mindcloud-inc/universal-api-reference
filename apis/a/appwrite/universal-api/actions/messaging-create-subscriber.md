# Appwrite: Create subscriber

Creates a new subscriber in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-create-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-create-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topicId": "string",
  "subscriberId": "string",
  "targetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-create-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topicId": "string",
    "subscriberId": "string",
    "targetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topicId` | string | yes | Topic ID. The topic ID to subscribe to. |
| `subscriberId` | string | yes | Subscriber ID. Choose a custom Subscriber ID or a new Subscriber ID. |
| `targetId` | string | yes | Target ID. The target ID to link to the specified Topic ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "providerType": "string",
      "target": {},
      "targetId": "string",
      "topicId": "string",
      "userId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Subscriber creation time in ISO 8601 format. |
| `$id` | string | Subscriber ID. |
| `$updatedAt` | string | Subscriber update date in ISO 8601 format. |
| `providerType` | string | The target provider type. Can be one of the following: `email`, `sms` or `push`. |
| `target` | object | Target. |
| `targetId` | string | Target ID. |
| `topicId` | string | Topic ID. |
| `userId` | string | Topic ID. |
| `userName` | string | User Name. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /messaging/topics/{topicId}/subscribers` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-create-subscriber.md) for the provider-specific parameters and requirements.


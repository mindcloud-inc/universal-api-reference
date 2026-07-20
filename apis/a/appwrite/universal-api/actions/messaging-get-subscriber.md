# Appwrite: Get subscriber

Retrieves the subscriber from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-get-subscriber?connectionId=$CONNECTION_ID&topicId=string&subscriberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topicId": "string",
  "subscriberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-get-subscriber?${params}`, {
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
| `topicId` | string | yes | Topic ID. The topic ID subscribed to. |
| `subscriberId` | string | yes | Subscriber ID. |

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

Through the native Appwrite API, this operation is `GET /messaging/topics/{topicId}/subscribers/{subscriberId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-get-subscriber.md) for the provider-specific parameters and requirements.


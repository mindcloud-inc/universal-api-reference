# Appwrite: Update topic

Updates the topic in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-update-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-update-topic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topicId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-update-topic', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topicId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscribe` | string | no | An array of role strings with subscribe permission. By default all users are granted with any subscribe permission. [learn more about roles](https://appwrite.io/docs/permissions#permission-roles). Maximum of 100 roles are allowed, each 64 characters long. |
| `topicId` | string | yes | Topic ID. |
| `name` | string | no | Topic Name. |
| `subscribe[]` | array<string> | no | An array of role strings with subscribe permission. By default all users are granted with any subscribe permission. [learn more about roles](https://appwrite.io/docs/permissions#permission-roles). Maximum of 100 roles are allowed, each 64 characters long. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "emailTotal": 1,
      "name": "Ava Chen",
      "pushTotal": 1,
      "smsTotal": 1,
      "subscribe": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Topic creation time in ISO 8601 format. |
| `$id` | string | Topic ID. |
| `$updatedAt` | string | Topic update date in ISO 8601 format. |
| `emailTotal` | number | Total count of email subscribers subscribed to the topic. |
| `name` | string | The name of the topic. |
| `pushTotal` | number | Total count of push subscribers subscribed to the topic. |
| `smsTotal` | number | Total count of SMS subscribers subscribed to the topic. |
| `subscribe` | array<string> | Subscribe permissions. |

## Native endpoint

Through the native Appwrite API, this operation is `PATCH /messaging/topics/{topicId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-update-topic.md) for the provider-specific parameters and requirements.


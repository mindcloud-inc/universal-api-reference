# Appwrite: Get topic

Retrieves the topic from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-get-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-get-topic?connectionId=$CONNECTION_ID&topicId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topicId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-get-topic?${params}`, {
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
| `topicId` | string | yes | Topic ID. |

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

Through the native Appwrite API, this operation is `GET /messaging/topics/{topicId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-get-topic.md) for the provider-specific parameters and requirements.


# Appwrite: Get message

Retrieves the message from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-get-message?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-get-message?${params}`, {
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
| `messageId` | string | yes | Message ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "data": {},
      "deliveredAt": "string",
      "deliveredTotal": 1,
      "deliveryErrors": [
        "string"
      ],
      "providerType": "string",
      "scheduledAt": "string",
      "status": "string",
      "targets": [
        "string"
      ],
      "topics": [
        "string"
      ],
      "users": [
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
| `$createdAt` | string | Message creation time in ISO 8601 format. |
| `$id` | string | Message ID. |
| `$updatedAt` | string | Message update date in ISO 8601 format. |
| `data` | object | Data of the message. |
| `deliveredAt` | string | The time when the message was delivered. |
| `deliveredTotal` | number | Number of recipients the message was delivered to. |
| `deliveryErrors` | array<string> | Delivery errors if any. |
| `providerType` | string | Message provider type. |
| `scheduledAt` | string | The scheduled time for message. |
| `status` | string | Status of delivery. |
| `targets` | array<string> | Target IDs set as recipients. |
| `topics` | array<string> | Topic IDs set as recipients. |
| `users` | array<string> | User IDs set as recipients. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /messaging/messages/{messageId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-get-message.md) for the provider-specific parameters and requirements.


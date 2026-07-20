# Dify: List App Feedbacks

Retrieves app feedback entries from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-app-feedbacks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-app-feedbacks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-app-feedbacks?${params}`, {
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
| `page` | number | no | Page number to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "content": "string",
      "conversationId": "string",
      "createdAt": "string",
      "fromAccountId": "string",
      "fromEndUserId": "string",
      "fromSource": "string",
      "id": "string",
      "messageId": "string",
      "rating": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `content` | string |  |
| `conversationId` | string |  |
| `createdAt` | string |  |
| `fromAccountId` | string |  |
| `fromEndUserId` | string |  |
| `fromSource` | string |  |
| `id` | string |  |
| `messageId` | string |  |
| `rating` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Dify API, this operation is `GET /app/feedbacks` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-app-feedbacks.md) for the provider-specific parameters and requirements.


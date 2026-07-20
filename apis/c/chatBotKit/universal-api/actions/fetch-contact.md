# ChatBotKit: Fetch Contact



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/fetch-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/fetch-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/fetch-contact?${params}`, {
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
| `contactId` | string | yes | The ID of the contact to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "description": "string",
      "email": "ava@example.com",
      "fingerprint": "string",
      "id": "string",
      "name": "Ava Chen",
      "nick": "string",
      "phone": "string",
      "preferences": "string",
      "updatedAt": 1,
      "verifiedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `description` | string |  |
| `email` | string |  |
| `fingerprint` | string |  |
| `id` | string |  |
| `name` | string |  |
| `nick` | string |  |
| `phone` | string |  |
| `preferences` | string |  |
| `updatedAt` | number |  |
| `verifiedAt` | number |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /contact/{contactId}/fetch` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-contact.md) for the provider-specific parameters and requirements.


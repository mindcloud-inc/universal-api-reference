# ChatBotKit: Retrieve File Details



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/retrieve-file-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/retrieve-file-details?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/retrieve-file-details?${params}`, {
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
| `fileId` | string | yes | The ID of the file to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blueprintId": "string",
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blueprintId` | string |  |
| `createdAt` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | number |  |
| `visibility` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /file/{fileId}/fetch` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-file-details.md) for the provider-specific parameters and requirements.


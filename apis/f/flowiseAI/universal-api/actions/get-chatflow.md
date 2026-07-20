# FlowiseAI: Get Chatflow

Retrieves a specific chatflow from FlowiseAI.

```
GET https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/get-chatflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/get-chatflow?connectionId=$CONNECTION_ID&id=d290f1ee-6c54-4b01-90e6-d701748f0851" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "d290f1ee-6c54-4b01-90e6-d701748f0851"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/get-chatflow?${params}`, {
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
| `id` | string | yes | Chatflow ID from the Flowise chatflows API. Example: `d290f1ee-6c54-4b01-90e6-d701748f0851`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analytic": "string",
      "apiConfig": "string",
      "apikeyid": "string",
      "category": "string",
      "chatbotConfig": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "deployed": true,
      "flowData": "string",
      "id": "string",
      "isPublic": true,
      "name": "Ava Chen",
      "speechToText": "string",
      "type": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analytic` | string |  |
| `apiConfig` | string |  |
| `apikeyid` | string |  |
| `category` | string |  |
| `chatbotConfig` | string |  |
| `createdDate` | date |  |
| `deployed` | boolean |  |
| `flowData` | string |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `speechToText` | string |  |
| `type` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native FlowiseAI API, this operation is `GET /chatflows/{id}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chatflow.md) for the provider-specific parameters and requirements.


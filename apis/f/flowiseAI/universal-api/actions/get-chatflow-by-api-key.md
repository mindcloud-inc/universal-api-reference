# FlowiseAI: Get Chatflow by API Key

Retrieves a FlowiseAI chatflow by API key.

```
GET https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/get-chatflow-by-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/get-chatflow-by-api-key?connectionId=$CONNECTION_ID&apikey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apikey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/get-chatflow-by-api-key?${params}`, {
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
| `apikey` | string | yes | API key associated with the Flowise chatflow. |

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

Through the native FlowiseAI API, this operation is `GET /chatflows/apikey/{apikey}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chatflow-by-api-key.md) for the provider-specific parameters and requirements.


# FlowiseAI: List Chatflows

Retrieves a list of chatflows from FlowiseAI.

```
GET https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-chatflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-chatflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-chatflows?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native FlowiseAI API, this operation is `GET /chatflows` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chatflows.md) for the provider-specific parameters and requirements.


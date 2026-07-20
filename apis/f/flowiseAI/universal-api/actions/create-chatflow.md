# FlowiseAI: Create Chatflow

Creates a new chatflow in FlowiseAI.

```
POST https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-chatflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-chatflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-chatflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON body with documented chatflow fields such as name, flowData, deployed, and isPublic. |

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

Through the native FlowiseAI API, this operation is `POST /chatflows` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chatflow.md) for the provider-specific parameters and requirements.


# FlowiseAI: Update Tool

Updates an existing tool in FlowiseAI.

```
PUT https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/update-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/update-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/update-tool', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON body with documented Flowise tool fields to update. |
| `id` | string | yes | Tool ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "func": "string",
      "iconSrc": "string",
      "id": "string",
      "name": "Ava Chen",
      "schema": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createdDate` | date |  |
| `description` | string |  |
| `func` | string |  |
| `iconSrc` | string |  |
| `id` | string |  |
| `name` | string |  |
| `schema` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native FlowiseAI API, this operation is `PUT /tools/{id}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tool.md) for the provider-specific parameters and requirements.


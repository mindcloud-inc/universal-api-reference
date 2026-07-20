# FlowiseAI: Get Tool

Retrieves a specific tool from FlowiseAI.

```
GET https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/get-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/get-tool?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/get-tool?${params}`, {
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
| `id` | string | yes | Tool ID. |

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

Through the native FlowiseAI API, this operation is `GET /tools/{id}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tool.md) for the provider-specific parameters and requirements.


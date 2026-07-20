# FlowiseAI: List Tools

Retrieves a list of tools from FlowiseAI.

```
GET https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-tools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-tools?${params}`, {
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

Through the native FlowiseAI API, this operation is `GET /tools` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tools.md) for the provider-specific parameters and requirements.


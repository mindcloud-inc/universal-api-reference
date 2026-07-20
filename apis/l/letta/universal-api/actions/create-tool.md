# Letta: Create Tool

Creates a new tool in Letta.

```
POST https://connect.mindcloud.co/v1/universal/letta/latest/actions/create-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Letta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/letta/latest/actions/create-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letta/latest/actions/create-tool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceCode` | string | yes | The source code of the function to create as a Letta tool. |
| `description` | string | no | Optional description for the tool. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Letta API, this operation is `POST /v1/tools/` (base URL `https://api.letta.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tool.md) for the provider-specific parameters and requirements.


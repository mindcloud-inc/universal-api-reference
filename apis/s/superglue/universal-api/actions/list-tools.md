# Superglue: List Tools

Retrieves tools from Superglue.

```
GET https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-tools?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-tools?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inputSchema": {},
      "instruction": "string",
      "outputTransform": "string",
      "steps": [
        {}
      ],
      "systemIds": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Tool creation timestamp. |
| `id` | string | Superglue tool identifier. |
| `inputSchema` | object | JSON schema for tool inputs. |
| `instruction` | string | Human-readable instruction describing what the tool does. |
| `outputTransform` | string | Optional output transformation expression. |
| `steps` | array<object> | Ordered execution steps that make up the tool. |
| `systemIds` | array<string> | System identifiers used by the tool. |
| `updatedAt` | date | Tool update timestamp. |

## Native endpoint

Through the native Superglue API, this operation is `GET /tools` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tools.md) for the provider-specific parameters and requirements.


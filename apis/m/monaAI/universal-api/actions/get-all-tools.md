# Mona AI: Get All Tools

Retrieves all tools from Mona AI.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-all-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-all-tools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-all-tools?${params}`, {
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
      "count": {
        "total": 1
      },
      "data": [
        {}
      ],
      "grouped": {},
      "tools": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | object | Tool counts by category. |
| `count.total` | number | Total number of tools. |
| `data` | array<object> | Tool records returned by Mona. |
| `grouped` | object | Tools grouped by category. |
| `tools` | array<string> | Tool names returned by Mona. |

## Native endpoint

Through the native Mona AI API, this operation is `POST /database/getAllTools` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-tools.md) for the provider-specific parameters and requirements.


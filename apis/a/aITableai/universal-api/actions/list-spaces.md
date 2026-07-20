# AITable.ai: List Spaces

Retrieves a list of spaces from AITable.ai.

```
GET https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-spaces?${params}`, {
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
      "spaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `spaces` | array<object> | Spaces visible to the authenticated user. |

## Native endpoint

Through the native AITable.ai API, this operation is `GET /fusion/v1/spaces` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spaces.md) for the provider-specific parameters and requirements.


# PromptLayer Run Agent: List Skill Collections

Retrieves skill collections from PromptLayer.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-skill-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-skill-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-skill-collections?${params}`, {
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
      "skillCollections": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `skillCollections` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `GET /api/public/v2/skill-collections` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-skill-collections.md) for the provider-specific parameters and requirements.


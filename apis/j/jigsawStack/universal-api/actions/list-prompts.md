# JigsawStack: List Prompts



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/list-prompts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/list-prompts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/list-prompts?${params}`, {
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
      "_usage": {},
      "has_more": true,
      "limit": 1,
      "log_id": "string",
      "page": 1,
      "prompt_engines": [
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
| `_usage` | object |  |
| `has_more` | boolean |  |
| `limit` | number |  |
| `log_id` | string |  |
| `page` | number |  |
| `prompt_engines` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native JigsawStack API, this operation is `GET /v1/prompt_engine` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-prompts.md) for the provider-specific parameters and requirements.


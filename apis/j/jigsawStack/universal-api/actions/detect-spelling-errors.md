# JigsawStack: Detect Spelling Errors



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/detect-spelling-errors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/detect-spelling-errors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/detect-spelling-errors?${params}`, {
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
      "auto_correct_text": "string",
      "log_id": "string",
      "misspellings": [
        {}
      ],
      "misspellings_found": true,
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
| `auto_correct_text` | string |  |
| `log_id` | string |  |
| `misspellings` | array<object> |  |
| `misspellings_found` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native JigsawStack API, this operation is `POST /v1/validate/spell_check` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-spelling-errors.md) for the provider-specific parameters and requirements.


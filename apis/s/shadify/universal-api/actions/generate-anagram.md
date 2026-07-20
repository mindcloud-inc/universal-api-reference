# Shadify: Generate Anagram

Retrieves a random anagram from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-anagram
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-anagram?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-anagram?${params}`, {
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
      "task": "string",
      "words": [
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
| `task` | string | Source word for the anagram. |
| `words` | array<string> | Possible words from the task word. |

## Native endpoint

Through the native Shadify API, this operation is `GET /anagram/generator` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-anagram.md) for the provider-specific parameters and requirements.


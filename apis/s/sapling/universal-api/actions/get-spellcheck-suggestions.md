# Sapling: Get Spellcheck Suggestions

Retrieves spellcheck suggestions for text from Sapling.

```
GET https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-spellcheck-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-spellcheck-suggestions?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-spellcheck-suggestions?${params}`, {
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
| `text` | string | yes | Text to check for spelling errors. |
| `sessionId` | string | no | Optional document or session identifier for the spellcheck request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "edits": [
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
| `edits` | array<object> | List of spellcheck suggestions. |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/spellcheck` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-spellcheck-suggestions.md) for the provider-specific parameters and requirements.


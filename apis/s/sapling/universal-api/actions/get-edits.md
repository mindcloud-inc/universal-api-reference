# Sapling: Get Edits

Retrieves grammar edits for text from Sapling.

```
GET https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-edits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-edits?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-edits?${params}`, {
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
| `text` | string | yes | Text to process for grammar, spelling, and stylistic edits. |
| `sessionId` | string | no | Optional document or session identifier for the text being checked. |

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
| `edits` | array<object> | List of suggested edits. |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/edits` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-edits.md) for the provider-specific parameters and requirements.


# Sapling: Get Autocomplete

Retrieves autocomplete suggestions for text from Sapling.

```
GET https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-autocomplete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-autocomplete?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-autocomplete?${params}`, {
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
| `query` | string | yes | Text that should be autocompleted. |
| `sessionId` | string | no | Document or session identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hash": "string",
      "output": "string",
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hash` | string |  |
| `output` | string |  |
| `query` | string |  |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/complete` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-autocomplete.md) for the provider-specific parameters and requirements.


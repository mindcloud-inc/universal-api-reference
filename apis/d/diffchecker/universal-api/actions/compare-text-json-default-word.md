# Diffchecker: Compare Text (JSON, Default Word)

Compares text in Diffchecker and returns a word-level JSON diff.

```
GET https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-text-json-default-word
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffchecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-text-json-default-word?connectionId=$CONNECTION_ID&left=string&right=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "left": "string",
  "right": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-text-json-default-word?${params}`, {
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
| `left` | string | yes | The left text to compare. |
| `right` | string | yes | The right text to compare. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": 1,
      "removed": 1,
      "rows": [
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
| `added` | number | Number of inserted chunks. |
| `removed` | number | Number of removed chunks. |
| `rows` | array<object> | Structured line-by-line diff rows. |

## Native endpoint

Through the native Diffchecker API, this operation is `POST /text` (base URL `https://api.diffchecker.com/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-text-json-default-word.md) for the provider-specific parameters and requirements.


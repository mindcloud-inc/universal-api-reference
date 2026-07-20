# Diffchecker: Compare Documents (JSON, Default Word, Uploads)

Compares documents in Diffchecker and returns a word-level JSON diff from uploads.

```
GET https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-documents-json-default-word-uploads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffchecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-documents-json-default-word-uploads?connectionId=$CONNECTION_ID&left_pdf=string&right_pdf=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "left_pdf": "string",
  "right_pdf": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-documents-json-default-word-uploads?${params}`, {
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
| `left_pdf` | file | yes | Left PDF upload. |
| `right_pdf` | file | yes | Right PDF upload. |

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
| `rows` | array<object> | Structured line-by-line PDF diff rows. |

## Native endpoint

Through the native Diffchecker API, this operation is `POST /pdf` (base URL `https://api.diffchecker.com/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-documents-json-default-word-uploads.md) for the provider-specific parameters and requirements.


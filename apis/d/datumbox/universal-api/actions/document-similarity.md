# Datumbox: Document Similarity

Compares two documents for similarity in Datumbox.

```
GET https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/document-similarity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datumbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/document-similarity?connectionId=$CONNECTION_ID&original=Enter%20the%20original%20clear-text%20document.&copy=Enter%20the%20comparison%20clear-text%20document." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "original": "Enter the original clear-text document.",
  "copy": "Enter the comparison clear-text document."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/document-similarity?${params}`, {
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
| `original` | string | yes | The first clear-text document to compare. Example: `Enter the original clear-text document.`. |
| `copy` | string | yes | The second clear-text document to compare. Example: `Enter the comparison clear-text document.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Similarity metrics returned for the two submitted documents. |
| `status` | number | Datumbox success flag for the operation. |

## Native endpoint

Through the native Datumbox API, this operation is `POST /DocumentSimilarity.json` (base URL `http://api.datumbox.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/document-similarity.md) for the provider-specific parameters and requirements.


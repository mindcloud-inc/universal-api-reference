# Smartcat: Delete Documents

Deletes documents from the current Smartcat account.

```
DELETE https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/delete-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/delete-documents?connectionId=$CONNECTION_ID&documentIds=abc_9%2Ca02_9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentIds": "abc_9,a02_9"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/delete-documents?${params}`, {
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
| `documentIds` | string | yes | One or more document IDs in documentId_targetLanguageId format Accepts multiple values in one string, delimited by `,`. Example: `abc_9,a02_9`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Smartcat API returns.

## Native endpoint

Through the native Smartcat API, this operation is `DELETE /api/integration/v1/document` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-documents.md) for the provider-specific parameters and requirements.


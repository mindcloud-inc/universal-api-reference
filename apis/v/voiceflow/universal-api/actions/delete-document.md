# Voiceflow: Delete Document

Deletes a knowledge base document from Voiceflow.

```
DELETE https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-document?connectionId=$CONNECTION_ID&documentId=69c5797e04502251683f7768" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "69c5797e04502251683f7768"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-document?${params}`, {
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
| `documentId` | string | yes | ID of the document to delete. Example: `69c5797e04502251683f7768`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `DELETE https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.


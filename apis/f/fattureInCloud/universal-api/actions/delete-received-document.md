# Fatture in Cloud: Delete Received Document

Deletes an existing received document from Fatture in Cloud.

```
DELETE https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/delete-received-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/delete-received-document?connectionId=$CONNECTION_ID&companyId=1&documentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1",
  "documentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/delete-received-document?${params}`, {
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
| `companyId` | number | yes | The ID of the company. |
| `documentId` | number | yes | The ID of the document. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fatture in Cloud API returns.

## Native endpoint

Through the native Fatture in Cloud API, this operation is `DELETE /c/:company_id/received_documents/:document_id` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-received-document.md) for the provider-specific parameters and requirements.


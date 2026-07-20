# Mendeley: Remove Document From Folder



```
DELETE https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/remove-document-from-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/remove-document-from-folder?connectionId=$CONNECTION_ID&id=ffb4e999-557c-40b7-8fc9-9b5d5c24847d&documentId=2531dfc9-90cd-3136-8001-abadb5929161" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "ffb4e999-557c-40b7-8fc9-9b5d5c24847d",
  "documentId": "2531dfc9-90cd-3136-8001-abadb5929161"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/remove-document-from-folder?${params}`, {
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
| `id` | string | yes | Identifier of the folder. Example: `ffb4e999-557c-40b7-8fc9-9b5d5c24847d`. |
| `documentId` | string | yes | Identifier of the document to remove from the folder. Example: `2531dfc9-90cd-3136-8001-abadb5929161`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mendeley API returns.

## Native endpoint

Through the native Mendeley API, this operation is `DELETE /folders/:id/documents/:document_id` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-document-from-folder.md) for the provider-specific parameters and requirements.


# Siteleaf: Delete Document

Deletes an existing document from Siteleaf.

```
DELETE https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/delete-document?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/delete-document?${params}`, {
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
| `documentId` | string | no | Siteleaf document identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |

## Native endpoint

Through the native Siteleaf API, this operation is `DELETE /documents/:document_id` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.


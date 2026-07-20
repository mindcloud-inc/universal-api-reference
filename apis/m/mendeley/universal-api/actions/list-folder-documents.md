# Mendeley: List Folder Documents



```
GET https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/list-folder-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/list-folder-documents?connectionId=$CONNECTION_ID&id=ffb4e999-557c-40b7-8fc9-9b5d5c24847d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "ffb4e999-557c-40b7-8fc9-9b5d5c24847d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/list-folder-documents?${params}`, {
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mendeley API returns.

## Native endpoint

Through the native Mendeley API, this operation is `GET /folders/:id/documents` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folder-documents.md) for the provider-specific parameters and requirements.


# Dart: Delete Doc

Deletes an existing doc from Dart.

```
DELETE https://connect.mindcloud.co/v1/universal/dart/latest/actions/delete-doc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dart/latest/actions/delete-doc?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dart/latest/actions/delete-doc?${params}`, {
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
| `id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": "string",
      "htmlUrl": "https://example.com",
      "id": "string",
      "text": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | string |  |
| `htmlUrl` | string |  |
| `id` | string |  |
| `text` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Dart API, this operation is `DELETE /docs/:id` (base URL `https://app.dartai.com/api/v0/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-doc.md) for the provider-specific parameters and requirements.


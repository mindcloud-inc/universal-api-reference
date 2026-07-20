# Happy SMS: Delete Document



```
DELETE https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Happy SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/delete-document?connectionId=$CONNECTION_ID&id=mindcloud-nonexistent-doc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "mindcloud-nonexistent-doc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/delete-document?${params}`, {
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
| `id` | string | yes | Unique document identifier. Default: `mindcloud-nonexistent-doc`. |

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
| `deleted` | boolean | Whether the document was deleted. |
| `id` | string | Identifier of the deleted document. |

## Native endpoint

Through the native Happy SMS API, this operation is `DELETE /api/v1/protected/domain/custom-data/documents/:id` (base URL `https://www.api.nc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.


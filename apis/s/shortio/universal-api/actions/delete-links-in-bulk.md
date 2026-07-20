# Short.io: Delete Links in Bulk

Deletes links in bulk from Short.io.

```
DELETE https://connect.mindcloud.co/v1/universal/shortio/latest/actions/delete-links-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/delete-links-in-bulk?connectionId=$CONNECTION_ID&linkIds%5B%5D=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkIds[]": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortio/latest/actions/delete-links-in-bulk?${params}`, {
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
| `linkIds[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Short.io API, this operation is `DELETE /links/delete_bulk` (base URL `https://api.short.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-links-in-bulk.md) for the provider-specific parameters and requirements.


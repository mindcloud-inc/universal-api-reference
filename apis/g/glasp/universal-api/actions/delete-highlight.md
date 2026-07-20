# Glasp: Delete Highlight

Deletes a Glasp highlight or all highlights in a document.

```
DELETE https://connect.mindcloud.co/v1/universal/glasp/latest/actions/delete-highlight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Glasp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/glasp/latest/actions/delete-highlight?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&highlightId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "highlightId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/glasp/latest/actions/delete-highlight?${params}`, {
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
| `url` | string | yes | Document URL that owns the highlight. |
| `highlightId` | string | yes | Identifier of the Glasp highlight to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "highlightId": "string",
        "url": "https://example.com"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Deletion payload returned by Glasp. |
| `data.highlightId` | string | Highlight identifier that Glasp deleted. |
| `data.url` | string | Source URL that owned the deleted highlight. |
| `message` | string | Deletion status message from Glasp. |

## Native endpoint

Through the native Glasp API, this operation is `DELETE /v1/highlights/delete` (base URL `https://api.glasp.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-highlight.md) for the provider-specific parameters and requirements.


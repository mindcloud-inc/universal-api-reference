# Recut URL Shortener: Delete Link

Deletes an existing link from Recut URL Shortener.

```
DELETE https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/delete-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/delete-link?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/delete-link?${params}`, {
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
| `id` | number | yes | Link ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number |  |
| `message` | string |  |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `DELETE /url/:id/delete` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-link.md) for the provider-specific parameters and requirements.


# TLY Link Shortener: Get Tag

Retrieves a tag from TLY Link Shortener.

```
GET https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-tag?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-tag?${params}`, {
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
| `id` | number | yes | The tag ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "tag": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | number |  |
| `tag` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `GET /api/v1/link/tag/:id` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.


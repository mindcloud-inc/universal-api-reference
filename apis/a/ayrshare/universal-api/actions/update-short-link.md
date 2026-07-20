# Ayrshare: Update Short Link

Updates a short link in Ayrshare.

```
PUT https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-short-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Ayrshare short link ID to update. |
| `url` | string | yes | New destination URL for the short link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "id": "string",
      "message": "string",
      "shortUrl": "https://example.com",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `id` | string | Short link ID. |
| `message` | string | Update link or error message. |
| `shortUrl` | string | Short URL. |
| `status` | string | Update short link status. |
| `url` | string | Destination URL. |

## Native endpoint

Through the native Ayrshare API, this operation is `PUT /links/:id` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-short-link.md) for the provider-specific parameters and requirements.


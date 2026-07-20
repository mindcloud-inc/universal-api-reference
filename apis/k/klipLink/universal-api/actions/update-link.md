# KlipLink: Update Link



```
PUT https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KlipLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shortUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shortUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shortUrl` | string | yes | The short URL identifier, for example klipl.ink/example. |
| `destinationUrl` | string | no | Optional new destination URL for the link. |
| `title` | string | no | Optional new title for the link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "destination_url": "https://example.com",
      "id": "string",
      "short_url": "https://example.com",
      "success": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number | Current click count for the link. |
| `created_at` | date | Creation timestamp for the link. |
| `destination_url` | string | Destination URL stored for the link. |
| `id` | string | KlipLink identifier for the link. |
| `short_url` | string | Short URL returned by KlipLink. |
| `success` | boolean | Whether the request succeeded. |
| `title` | string | Title for the link. |

## Native endpoint

Through the native KlipLink API, this operation is `PUT /v1/links/:short_url` (base URL `https://api.klipl.ink`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.


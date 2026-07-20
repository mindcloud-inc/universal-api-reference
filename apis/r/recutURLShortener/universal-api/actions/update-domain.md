# Recut URL Shortener: Update Domain

Updates an existing branded domain in Recut URL Shortener.

```
PUT https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Domain ID Example: `1`. |
| `redirectRoot` | string | no | Redirect URL for the domain root Example: `https://example.com`. |
| `redirect404` | string | no | Redirect URL for 404 pages Example: `https://example.com/not-found`. |

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

Through the native Recut URL Shortener API, this operation is `PUT /domain/:id/update` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-domain.md) for the provider-specific parameters and requirements.


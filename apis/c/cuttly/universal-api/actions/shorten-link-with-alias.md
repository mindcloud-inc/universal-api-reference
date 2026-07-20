# Cutt.ly: Shorten Link With Alias

Creates a shortened link with a custom alias in Cutt.ly.

```
POST https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/shorten-link-with-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cutt.ly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/shorten-link-with-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "short": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/shorten-link-with-alias', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "short": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `short` | string | yes | The full destination URL to shorten. |
| `name` | string | yes | Requested short-link alias. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "fullLink": "https://example.com",
      "shortLink": "https://example.com",
      "status": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string | Short-link creation date from the provider response. |
| `fullLink` | string | Original destination URL. |
| `shortLink` | string | Generated or existing shortened URL. |
| `status` | number | Provider status code for the shortening operation. |
| `title` | string | Resolved title for the destination page when available. |

## Native endpoint

Through the native Cutt.ly API, this operation is `GET /api.php` (base URL `https://cutt.ly/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/shorten-link-with-alias.md) for the provider-specific parameters and requirements.


# Docubee: Generate Short URL

Generates a temporary short URL for a Docubee link.

```
POST https://connect.mindcloud.co/v1/universal/docubee/latest/actions/generate-short-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/generate-short-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docubee/latest/actions/generate-short-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | no | The full Docubee URL to shorten. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires` | string | When the short URL expires. |
| `url` | string | The generated short URL. |

## Native endpoint

Through the native Docubee API, this operation is `POST /urls` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-short-url.md) for the provider-specific parameters and requirements.


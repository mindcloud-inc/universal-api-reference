# LLMLayer: Map Website with Subdomains

Retrieves discovered website and subdomain URLs from LLMLayer.

```
GET https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/map-website-with-subdomains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/map-website-with-subdomains?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/map-website-with-subdomains?${params}`, {
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
| `url` | string | yes | Website URL to map. Example: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "links": [
        {}
      ],
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number | LLMLayer request cost. |
| `links` | array<object> | Mapped website links. |
| `statusCode` | number | HTTP status code returned by the mapping request. |

## Native endpoint

Through the native LLMLayer API, this operation is `POST /api/v2/map` (base URL `https://api.llmlayer.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/map-website-with-subdomains.md) for the provider-specific parameters and requirements.


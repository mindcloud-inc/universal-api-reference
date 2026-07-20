# Host.io: Get Domain Web Metadata

Retrieves web metadata for a domain from Host.io.

```
GET https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-web-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Host.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-web-metadata?connectionId=$CONNECTION_ID&domain=facebook.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "facebook.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-web-metadata?${params}`, {
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
| `domain` | string | yes | Domain to retrieve homepage metadata for. Default: `facebook.com`. Example: `facebook.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "copyright": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domain": "string",
      "encoding": "string",
      "ip": "string",
      "length": 1,
      "links": [
        "https://example.com"
      ],
      "rank": 1,
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `copyright` | string | Scraped copyright notice. |
| `date` | date | Date metadata was scraped. |
| `description` | string | HTML meta description. |
| `domain` | string | Domain name. |
| `encoding` | string | Detected page encoding. |
| `ip` | string | Scraped IP address. |
| `length` | number | HTML content length. |
| `links` | array<string> | Domains linked from the homepage. |
| `rank` | number | Host.io rank. |
| `title` | string | HTML title. |
| `url` | string | Homepage URL. |

## Native endpoint

Through the native Host.io API, this operation is `GET /web/:domain` (base URL `https://host.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-web-metadata.md) for the provider-specific parameters and requirements.


# Shorten.REST: List Clicks

Retrieves raw click data from Shorten.REST.

```
GET https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/list-clicks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shorten.REST `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/list-clicks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/list-clicks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "aliasId": "string",
      "browser": "string",
      "country": "string",
      "createdAt": 1,
      "destination": "string",
      "domain": "string",
      "os": "string",
      "referrer": "string",
      "userAgent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | Alias that received the click. |
| `aliasId` | string | Unique alias identifier. |
| `browser` | string | Detected browser. |
| `country` | string | ISO alpha-2 country code when available. |
| `createdAt` | number | Click timestamp in milliseconds. |
| `destination` | string | Resolved destination URL. |
| `domain` | string | Domain used for the short link. |
| `os` | string | Detected operating system. |
| `referrer` | string | HTTP referrer when present. |
| `userAgent` | string | Raw user agent string. |

## Native endpoint

Through the native Shorten.REST API, this operation is `GET /clicks` (base URL `https://api.shorten.rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clicks.md) for the provider-specific parameters and requirements.


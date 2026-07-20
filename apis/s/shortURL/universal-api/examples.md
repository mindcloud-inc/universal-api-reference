# Short URL Universal API Examples

These examples use the MindCloud API key and Short URL connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/get-account-info?connectionId=$CONNECTION_ID&baseDomain=surl.link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseDomain": "surl.link"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/get-account-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "isPaid": "string",
      "remainingUrls": "https://example.com",
      "response": "string",
      "responseCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shortURL/latest/actions/get-account-info).

## Create Short URL

Creates a new short URL in Short URL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/create-short-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseDomain": "surl.link",
  "longUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/create-short-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseDomain": "surl.link",
    "longUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "response": "string",
      "responseCode": "string",
      "shortUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Short URL action reference](actions/create-short-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shortURL/latest/actions/create-short-url).

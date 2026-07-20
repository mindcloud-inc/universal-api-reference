# Rakuten Advertising Universal API Examples

These examples use the MindCloud API key and Rakuten Advertising connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List advertisers

Retrieves advertisers from Rakuten Advertising.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-advertisers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-advertisers?${params}`, {
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
      "categories": [
        "string"
      ],
      "description": "string",
      "id": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "network": "string",
      "policies": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List advertisers action reference](actions/list-advertisers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rakutenAdvertising/latest/actions/list-advertisers).

## Create deep link

Creates a deep link in Rakuten Advertising.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/create-deep-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "advertiserId": 1,
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/create-deep-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "advertiserId": 1,
    "url": "https://example.com"
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
      "advertiserId": "string",
      "deepLinkUrl": "https://example.com",
      "message": "string",
      "success": true,
      "u1": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create deep link action reference](actions/create-deep-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rakutenAdvertising/latest/actions/create-deep-link).

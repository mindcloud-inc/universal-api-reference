# Reddit Lead Ads Universal API Examples

These examples use the MindCloud API key and Reddit Lead Ads connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Me

Retrieves the authenticated user from Reddit Ads.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-me?${params}`, {
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
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "lastname": "Chen",
      "phone": "string",
      "redditUsername": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Me action reference](actions/get-me.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/redditAds/latest/actions/get-me).

## Create Ad

Creates an ad in Reddit Ads.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/create-ad" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "adAccountId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/create-ad', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "adAccountId": "string",
    "data": {}
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
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Ad action reference](actions/create-ad.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/redditAds/latest/actions/create-ad).

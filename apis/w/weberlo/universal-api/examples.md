# Weberlo Universal API Examples

These examples use the MindCloud API key and Weberlo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Websites

Retrieves a list of websites from Weberlo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/list-websites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/list-websites?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Websites action reference](actions/list-websites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weberlo/latest/actions/list-websites).

## Create Ad Channel

Creates an ad channel in Weberlo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-ad-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Meta Ads",
  "icon": "https://example.com/ad-channel.png",
  "adPlatform": "facebook",
  "adAccountId": "1234567890"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-ad-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Meta Ads",
    "icon": "https://example.com/ad-channel.png",
    "adPlatform": "facebook",
    "adAccountId": "1234567890"
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
      "adAccountId": "string",
      "adAccountPlatform": "string",
      "icon": "string",
      "id": "string",
      "name": "Ava Chen",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Ad Channel action reference](actions/create-ad-channel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weberlo/latest/actions/create-ad-channel).

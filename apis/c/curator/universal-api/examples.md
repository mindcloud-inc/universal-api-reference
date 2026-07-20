# Curator Universal API Examples

These examples use the MindCloud API key and Curator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Feeds

Retrieves feeds from Curator.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-feeds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-feeds?${params}`, {
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
      "apiId": "string",
      "cacheTime": 1,
      "id": "string",
      "isLatestVersion": true,
      "moderation": "string",
      "name": "Ava Chen",
      "postCount": 1,
      "postStatus": 1,
      "publicKey": "string",
      "slug": "string",
      "type": "string",
      "widgetTheme": "string",
      "widgetType": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Feeds action reference](actions/list-feeds.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/curator/latest/actions/list-feeds).

## Create Ad

Creates an ad or custom post in Curator.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-ad" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedId": "string",
  "networkId": 1,
  "name": "Ava Chen",
  "positionStart": 1,
  "positionRepeats": true,
  "text": "string",
  "status": "string",
  "clickAction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-ad', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedId": "string",
    "networkId": 1,
    "name": "Ava Chen",
    "positionStart": 1,
    "positionRepeats": true,
    "text": "string",
    "status": "string",
    "clickAction": "string"
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
      "clickAction": "string",
      "feedId": "string",
      "id": "string",
      "name": "Ava Chen",
      "networkId": 1,
      "networkName": "Ava Chen",
      "positionRepeatInterval": 1,
      "positionRepeats": true,
      "positionStart": 1,
      "slug": "string",
      "status": "string",
      "text": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Ad action reference](actions/create-ad.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/curator/latest/actions/create-ad).

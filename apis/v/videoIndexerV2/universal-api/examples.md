# Video Indexer (V2) Universal API Examples

These examples use the MindCloud API key and Video Indexer (V2) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Accounts

Retrieves accounts from Video Indexer (V2).

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/get-accounts?${params}`, {
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
      "accessToken": {},
      "accountType": "string",
      "id": "string",
      "location": "string",
      "moveToArmStartedDate": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Accounts action reference](actions/get-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/videoIndexerV2/latest/actions/get-accounts).

## Re-Index Video

Re-indexes a video in Video Indexer (V2).

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/re-index-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "location": "string",
  "accountId": "string",
  "videoId": "string",
  "accessToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/videoIndexerV2/latest/actions/re-index-video', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "location": "string",
    "accountId": "string",
    "videoId": "string",
    "accessToken": "string"
  })
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

See the full [Re-Index Video action reference](actions/re-index-video.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/videoIndexerV2/latest/actions/re-index-video).

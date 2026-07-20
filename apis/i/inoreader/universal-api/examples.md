# Inoreader Universal API Examples

These examples use the MindCloud API key and Inoreader connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Information

Retrieves the current user information from Inoreader.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/get-user-information?${params}`, {
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
      "isBloggerUser": true,
      "isMultiLoginEnabled": true,
      "signupTimeSec": 1,
      "userEmail": "ava@example.com",
      "userId": "string",
      "userName": "Ava Chen",
      "userProfileId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Information action reference](actions/get-user-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inoreader/latest/actions/get-user-information).

## Add Feed

Adds a new feed subscription in Inoreader.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/add-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/add-feed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedUrl": "https://example.com"
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
      "numResults": 1,
      "query": "string",
      "streamId": "string",
      "streamName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add Feed action reference](actions/add-feed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inoreader/latest/actions/add-feed).

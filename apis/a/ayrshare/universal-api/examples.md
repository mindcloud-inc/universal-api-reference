# Ayrshare Universal API Examples

These examples use the MindCloud API key and Ayrshare connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Profile Details

Retrieves user profile details from Ayrshare.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-user-profile-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-user-profile-details?${params}`, {
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
      "activeSocialAccounts": [
        "string"
      ],
      "created": {},
      "email": "ava@example.com",
      "lastApiCall": "2026-05-07T12:00:00.000Z",
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "linkedSocialAccounts": [
        "https://example.com"
      ],
      "monthlyApiCalls": 1,
      "monthlyPostCount": 1,
      "monthlyPostQuota": 1,
      "nextUpdate": "2026-05-07T12:00:00.000Z",
      "refId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Profile Details action reference](actions/get-user-profile-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ayrshare/latest/actions/get-user-profile-details).

## Add RSS Feed

Creates a new RSS feed in Ayrshare.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/add-rss-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "platforms[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/add-rss-feed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "platforms[]": ["string"]
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
      "code": 1,
      "id": "string",
      "message": "string",
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add RSS Feed action reference](actions/add-rss-feed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ayrshare/latest/actions/add-rss-feed).

# Lnk.Bio Universal API Examples

These examples use the MindCloud API key and Lnk.Bio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Basic Profile Info

Retrieves the authenticated user's profile from Lnk.Bio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/retrieve-basic-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/retrieve-basic-profile-info?${params}`, {
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
      "errors": [
        "string"
      ],
      "info": {
        "profile_pic": "string",
        "url": "https://example.com",
        "username": "Ava Chen"
      },
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Basic Profile Info action reference](actions/retrieve-basic-profile-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lnkBio/latest/actions/retrieve-basic-profile-info).

## Create Lnk

Creates a new Lnk in Lnk.Bio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/create-lnk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "link": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/create-lnk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "link": "https://example.com"
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
      "data": {
        "id": 1,
        "url": "https://example.com"
      },
      "errors": [
        "string"
      ],
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Create Lnk action reference](actions/create-lnk.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lnkBio/latest/actions/create-lnk).

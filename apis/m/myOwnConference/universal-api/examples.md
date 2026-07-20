# MyOwnConference Universal API Examples

These examples use the MindCloud API key and MyOwnConference connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get profile

Retrieves the current MyOwnConference account profile.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myOwnConference/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myOwnConference/latest/actions/get-profile?${params}`, {
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
      "company": "string",
      "email": "ava@example.com",
      "gateway": "string",
      "language": "string",
      "name": "Ava Chen",
      "subscribe": "string",
      "timemove": "string",
      "timezone": 1
    }
  ],
  "meta": {}
}
```

See the full [Get profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/myOwnConference/latest/actions/get-profile).

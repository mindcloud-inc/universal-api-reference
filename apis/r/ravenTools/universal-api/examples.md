# Raven Tools Universal API Examples

These examples use the MindCloud API key and Raven Tools connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile Info

Retrieves profile details from Raven Tools.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/get-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/get-profile-info?${params}`, {
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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Profile Info action reference](actions/get-profile-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ravenTools/latest/actions/get-profile-info).

## Activate Link

Updates a link to active in Raven Tools.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/activate-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "link": "JSON array with one Raven link record including link id and status set to active."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/activate-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "link": "JSON array with one Raven link record including link id and status set to active."
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

See the full [Activate Link action reference](actions/activate-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ravenTools/latest/actions/activate-link).

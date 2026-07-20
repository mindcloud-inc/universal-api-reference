# Pastebin Universal API Examples

These examples use the MindCloud API key and Pastebin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Details

Retrieves the current Pastebin user's account details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/get-current-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/get-current-user-details?${params}`, {
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

See the full [Get Current User Details action reference](actions/get-current-user-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pastebin/latest/actions/get-current-user-details).

## Create Guest Paste

Creates a guest paste in Pastebin.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/create-guest-paste" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pasteContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/create-guest-paste', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pasteContent": "string"
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

See the full [Create Guest Paste action reference](actions/create-guest-paste.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pastebin/latest/actions/create-guest-paste).

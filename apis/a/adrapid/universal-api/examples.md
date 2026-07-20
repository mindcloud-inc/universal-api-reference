# Adrapid Universal API Examples

These examples use the MindCloud API key and Adrapid connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Whitelabel

Retrieves current whitelabel settings from Adrapid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/get-whitelabel?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/get-whitelabel?${params}`, {
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

See the full [Get Whitelabel action reference](actions/get-whitelabel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/adrapid/latest/actions/get-whitelabel).

## Create Group

Creates a new group in Adrapid.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Create Group action reference](actions/create-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/adrapid/latest/actions/create-group).

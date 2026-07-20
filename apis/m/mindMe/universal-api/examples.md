# MindMe Universal API Examples

These examples use the MindCloud API key and MindMe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Access Token

Retrieves an access token from MindMe.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/get-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/get-access-token?${params}`, {
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

See the full [Get Access Token action reference](actions/get-access-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mindMe/latest/actions/get-access-token).

## Add Contacts To Sequence

Adds contacts to a sequence in MindMe.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/add-contacts-to-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/add-contacts-to-sequence', {
  method: 'PUT',
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

See the full [Add Contacts To Sequence action reference](actions/add-contacts-to-sequence.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mindMe/latest/actions/add-contacts-to-sequence).

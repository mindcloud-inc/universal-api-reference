# Smoove Universal API Examples

These examples use the MindCloud API key and Smoove connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Active Contacts

Retrieves active contacts from Smoove.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-active-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-active-contacts?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Active Contacts action reference](actions/list-active-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smoove/latest/actions/list-active-contacts).

## Create Campaign

Creates a new email campaign in Smoove.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smoove/latest/actions/create-campaign', {
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
  "data": [
    {
      "customUnsubscribeMode": "string",
      "id": 1,
      "subject": "string",
      "trackLinks": true
    }
  ],
  "meta": {}
}
```

See the full [Create Campaign action reference](actions/create-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smoove/latest/actions/create-campaign).

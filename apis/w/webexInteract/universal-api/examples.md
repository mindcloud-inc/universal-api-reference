# Webex Interact Universal API Examples

These examples use the MindCloud API key and Webex Interact connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve account metadata

Retrieves account metadata from Webex Interact.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-account-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-account-metadata?${params}`, {
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
      "account_balance": 1,
      "account_status": "string",
      "account_uid": "string",
      "created": "string",
      "default_currency": "string",
      "home_region": "string",
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve account metadata action reference](actions/retrieve-account-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webexInteract/latest/actions/retrieve-account-metadata).

## Create contact list

Creates a new contact list in Webex Interact.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/create-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/create-contact-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create contact list action reference](actions/create-contact-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webexInteract/latest/actions/create-contact-list).

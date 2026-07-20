# Blooio Messaging Universal API Examples

These examples use the MindCloud API key and Blooio Messaging connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Authentication Context

Retrieves the current authentication context from Blooio Messaging.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-current-authentication-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-current-authentication-context?${params}`, {
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
      "apiKey": "string",
      "authType": "string",
      "devices": [
        {}
      ],
      "integrationDetails": {},
      "metadata": {},
      "organization": {},
      "organizationId": "string",
      "usage": {},
      "valid": true
    }
  ],
  "meta": {}
}
```

See the full [Get Current Authentication Context action reference](actions/get-current-authentication-context.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blooioMessaging/latest/actions/get-current-authentication-context).

## Add Contact Tags

Adds tags to a contact in Blooio Messaging.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/add-contact-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/add-contact-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string"
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
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Contact Tags action reference](actions/add-contact-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blooioMessaging/latest/actions/add-contact-tags).

# Trustmary Universal API Examples

These examples use the MindCloud API key and Trustmary connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test API Key

Retrieves API key test results from Trustmary.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/test-api-key?${params}`, {
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
      "api_key_name": "Ava Chen",
      "message": "string",
      "organization_id": "string",
      "organization_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Test API Key action reference](actions/test-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trustmary/latest/actions/test-api-key).

## Create or Update Contact

Finds a contact by email in Trustmary, or creates one if missing.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/create-or-update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/create-or-update-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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

See the full [Create or Update Contact action reference](actions/create-or-update-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trustmary/latest/actions/create-or-update-contact).

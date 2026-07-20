# gyfti Universal API Examples

These examples use the MindCloud API key and gyfti connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Credentials

Verifies gyfti API credentials with an access token.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/verify-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/verify-credentials?${params}`, {
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
      "state": "string",
      "user": {
        "_id": "string",
        "Company": "string",
        "Role": "string",
        "Status": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Verify Credentials action reference](actions/verify-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gyfti/latest/actions/verify-credentials).

## Add Contact to Email Campaign

Adds a contact to an email campaign in gyfti.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-contact-to-email-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign": "string",
  "contactEmail": "ava@example.com",
  "contactFirstname": "Ava",
  "contactLastname": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-contact-to-email-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaign": "string",
    "contactEmail": "ava@example.com",
    "contactFirstname": "Ava",
    "contactLastname": "Chen"
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
      "response": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contact to Email Campaign action reference](actions/add-contact-to-email-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gyfti/latest/actions/add-contact-to-email-campaign).

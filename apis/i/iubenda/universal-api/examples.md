# iubenda Universal API Examples

These examples use the MindCloud API key and iubenda connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Subjects

Retrieves subjects from iubenda.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-subjects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-subjects?${params}`, {
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
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": "string",
      "last_name": "Chen",
      "owner_id": "string",
      "preferences": {},
      "timestamp": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

See the full [List Subjects action reference](actions/list-subjects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iubenda/latest/actions/list-subjects).

## Create Consent

Creates a consent in iubenda.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-consent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-consent', {
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
      "id": "string",
      "subject_id": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Consent action reference](actions/create-consent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iubenda/latest/actions/create-consent).

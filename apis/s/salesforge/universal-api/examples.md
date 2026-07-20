# Salesforge Universal API Examples

These examples use the MindCloud API key and Salesforge connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact

Retrieves a contact from Salesforge.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-contact?connectionId=$CONNECTION_ID&workspaceId=wks_lxxtq91neaixc8yaiqp7w&contactId=lead_n539nxku3oq5k3w1cc5py" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "wks_lxxtq91neaixc8yaiqp7w",
  "contactId": "lead_n539nxku3oq5k3w1cc5py"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-contact?${params}`, {
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
      "company": "string",
      "customVars": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "linkedinUrl": "https://example.com",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Contact action reference](actions/get-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesforge/latest/actions/get-contact).

## Assign Contacts To Sequence

Assigns contacts to a sequence in Salesforge.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/assign-contacts-to-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
  "sequenceID": "seq_q266pc1d33ozbe3et0mes",
  "contactIds[]": "cnt_123456"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/assign-contacts-to-sequence', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
    "sequenceID": "seq_q266pc1d33ozbe3et0mes",
    "contactIds[]": "cnt_123456"
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

See the full [Assign Contacts To Sequence action reference](actions/assign-contacts-to-sequence.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesforge/latest/actions/assign-contacts-to-sequence).

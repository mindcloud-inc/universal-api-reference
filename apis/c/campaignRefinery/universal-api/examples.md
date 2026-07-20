# Campaign Refinery Universal API Examples

These examples use the MindCloud API key and Campaign Refinery connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contacts

Retrieves all contacts from Campaign Refinery.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-contacts?${params}`, {
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
      "_metadata": {
        "total_count": 1
      },
      "contacts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Contacts action reference](actions/get-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/campaignRefinery/latest/actions/get-contacts).

## Add Form to Contact

Adds a form to a contact in Campaign Refinery.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/add-form-to-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/add-form-to-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "formId": "string"
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

See the full [Add Form to Contact action reference](actions/add-form-to-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/campaignRefinery/latest/actions/add-form-to-contact).

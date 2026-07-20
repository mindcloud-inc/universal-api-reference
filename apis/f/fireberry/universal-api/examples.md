# Fireberry Universal API Examples

These examples use the MindCloud API key and Fireberry connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves all contact records from Fireberry.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireberry/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireberry/latest/actions/list-contacts?${params}`, {
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
      "accountid": "string",
      "accountname": "Ava Chen",
      "contactid": "string",
      "createdby": "string",
      "createdbyname": "Ava Chen",
      "createdon": "2026-05-07T12:00:00.000Z",
      "department": "string",
      "description": "string",
      "emailaddress1": "ava@example.com",
      "firstname": "Ava",
      "fullname": "Ava Chen",
      "isvalidforemail": "ava@example.com",
      "isvalidforemailcode": 1,
      "jobtitle": "string",
      "lastname": "Chen",
      "mobilephone1": "string",
      "modifiedby": "string",
      "modifiedbyname": "Ava Chen",
      "modifiedon": "2026-05-07T12:00:00.000Z",
      "ownerid": "string",
      "ownername": "Ava Chen",
      "salutation": "string",
      "salutationname": "Ava Chen",
      "telephone1": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fireberry/latest/actions/list-contacts).

# Growby Universal API Examples

These examples use the MindCloud API key and Growby connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from Growby.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growby/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growby/latest/actions/list-contacts?${params}`, {
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
      "accountId": 1,
      "address": "string",
      "anniversaryDate": {},
      "birthdate": {},
      "city": "string",
      "column1": "string",
      "column10": "string",
      "column11": "string",
      "column12": "string",
      "column13": "string",
      "column14": "string",
      "column15": "string",
      "column2": "string",
      "column3": "string",
      "column4": "string",
      "column5": "string",
      "column6": "string",
      "column7": "string",
      "column8": "string",
      "column9": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "countryCode": 1,
      "customerIdPartition": 1,
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isSubscribed": 1,
      "lastName": "Chen",
      "middleName": "Ava Chen",
      "mobileNumber": "string",
      "nationalNumber": "string",
      "nickName": "Ava Chen",
      "source": "string",
      "state": "string",
      "website": "string",
      "weddingDate": {},
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/growby/latest/actions/list-contacts).

## Add Contact To Group By Group ID

Adds a contact to a Growby group by group ID.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growby/latest/actions/add-contact-to-group-by-group-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": 1,
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growby/latest/actions/add-contact-to-group-by-group-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": 1,
    "contactId": 1
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

See the full [Add Contact To Group By Group ID action reference](actions/add-contact-to-group-by-group-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/growby/latest/actions/add-contact-to-group-by-group-id).

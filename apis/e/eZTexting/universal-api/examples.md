# EZ Texting Universal API Examples

These examples use the MindCloud API key and EZ Texting connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credit Balance

Retrieves account credit balance from EZ Texting.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/get-credit-balance?${params}`, {
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
      "anytimeCredits": 1,
      "planCredits": 1,
      "totalCredits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credit Balance action reference](actions/get-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eZTexting/latest/actions/get-credit-balance).

## Add Contacts to Contact Group

Adds contacts to a contact group in EZ Texting.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/add-contacts-to-contact-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "phoneNumbers[]": "(737) 337-8315"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/add-contacts-to-contact-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "phoneNumbers[]": "(737) 337-8315"
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
      "value0": "string",
      "value1": "string",
      "value10": "string",
      "value2": "string",
      "value3": "string",
      "value4": "string",
      "value5": "string",
      "value6": "string",
      "value7": "string",
      "value8": "string",
      "value9": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contacts to Contact Group action reference](actions/add-contacts-to-contact-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eZTexting/latest/actions/add-contacts-to-contact-group).

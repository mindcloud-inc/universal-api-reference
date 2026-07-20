# EasyBroker Universal API Examples

These examples use the MindCloud API key and EasyBroker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Property Types

Retrieves property types from EasyBroker.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/list-property-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/list-property-types?${params}`, {
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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Property Types action reference](actions/list-property-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyBroker/latest/actions/list-property-types).

## Create Contact Request

Creates or updates a property contact request in EasyBroker.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-contact-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyId": "string",
  "name": "Ava Chen",
  "message": "string",
  "source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-contact-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyId": "string",
    "name": "Ava Chen",
    "message": "string",
    "source": "string"
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

See the full [Create Contact Request action reference](actions/create-contact-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyBroker/latest/actions/create-contact-request).

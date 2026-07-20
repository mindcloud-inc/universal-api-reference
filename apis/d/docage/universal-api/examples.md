# Docage Universal API Examples

These examples use the MindCloud API key and Docage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves accessible organizations from Docage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-organizations?${params}`, {
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
      "Address1": "string",
      "City": "string",
      "Country": "string",
      "IntegratorId": "string",
      "IsDemo": true,
      "IsDeveloper": true,
      "Language": 1,
      "Name": "Ava Chen",
      "OrganizationStatus": 1,
      "OrganizationType": 1,
      "Phone": "string",
      "State": "string",
      "ZipCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docage/latest/actions/list-organizations).

## Create Box

Creates a new box in Docage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docage/latest/actions/create-box" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docage/latest/actions/create-box', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Box action reference](actions/create-box.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docage/latest/actions/create-box).

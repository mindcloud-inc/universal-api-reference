# Recreation.gov Universal API Examples

These examples use the MindCloud API key and Recreation.gov connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Public Organizations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-public-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-public-organizations?${params}`, {
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
      "children": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "parent_id": "string",
      "path": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Public Organizations action reference](actions/list-public-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recreationgov/latest/actions/list-public-organizations).

## Create Facility

Creates a new facility in Recreation.gov.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/create-facility" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "description": "string",
  "directions": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/create-facility', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "name": "Ava Chen",
    "description": "string",
    "description": "string",
    "directions": "string",
    "directions": "string"
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
      "MESSAGE": "string",
      "STATUSCODE": 1,
      "SUCCESS": true
    }
  ],
  "meta": {}
}
```

See the full [Create Facility action reference](actions/create-facility.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recreationgov/latest/actions/create-facility).

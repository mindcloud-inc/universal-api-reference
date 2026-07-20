# Fibery Universal API Examples

These examples use the MindCloud API key and Fibery connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Schema

Retrieves a schema from Fibery.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/get-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fibery/latest/actions/get-schema?${params}`, {
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
      "result": {
        "fibery/id": "string",
        "fibery/meta": {
          "fibery/rel-version": "string",
          "fibery/version": "string"
        },
        "fibery/types": [
          {
            "fibery/deleted?": true,
            "fibery/fields": [
              {
                "fibery/deleted?": true,
                "fibery/id": "string",
                "fibery/meta": {
                  "fibery/id?": true,
                  "fibery/readonly?": true,
                  "fibery/required?": true,
                  "fibery/secured?": true
                },
                "fibery/name": "Ava Chen",
                "fibery/type": "string"
              }
            ],
            "fibery/id": "string",
            "fibery/meta": {
              "fibery/domain?": true,
              "fibery/platform?": true,
              "fibery/primitive?": true,
              "fibery/secured?": true,
              "ui/color": "string"
            },
            "fibery/name": "Ava Chen"
          }
        ],
        "fibery/version": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Schema action reference](actions/get-schema.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fibery/latest/actions/get-schema).

## Add Collection Items

Adds collection items to an entity in Fibery.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/add-collection-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "field": "string",
  "entity": {},
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fibery/latest/actions/add-collection-items', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "field": "string",
    "entity": {},
    "items[]": [{}]
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
      "result": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Collection Items action reference](actions/add-collection-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fibery/latest/actions/add-collection-items).

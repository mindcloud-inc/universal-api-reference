# SalesRender Universal API Examples

These examples use the MindCloud API key and SalesRender connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from SalesRender.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-customers?connectionId=$CONNECTION_ID&query=query%20%7B%20customersFetcher%20%7B%20customers%20%7B%20id%20email%20registeredAt%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { customersFetcher { customers { id email registeredAt } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-customers?${params}`, {
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
      "data": {
        "customersFetcher": {
          "customers": [
            {
              "email": "ava@example.com",
              "id": "string",
              "registeredAt": "2026-05-07T12:00:00.000Z"
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesRender/latest/actions/list-customers).

## Create Item

Creates a new item in SalesRender.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation CreateItem($input: AddItemInput!) {\n  itemMutation {\n    addItem(input: $input) {\n      id\n      name\n      units\n      archived\n    }\n  }\n}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation CreateItem($input: AddItemInput!) {\n  itemMutation {\n    addItem(input: $input) {\n      id\n      name\n      units\n      archived\n    }\n  }\n}"
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
      "data": {
        "itemMutation": {
          "addItem": {
            "archived": true,
            "id": "string",
            "name": "Ava Chen",
            "units": "string"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Item action reference](actions/create-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesRender/latest/actions/create-item).

# EasyPost Universal API Examples

These examples use the MindCloud API key and EasyPost connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Shipments

Retrieves a list of shipments from EasyPost.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-shipments?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "mode": "string",
      "object": "string",
      "postageLabel": {},
      "rates": [
        {}
      ],
      "selectedRate": {},
      "status": "string",
      "tracker": {},
      "trackingCode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Shipments action reference](actions/list-shipments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyPost/latest/actions/list-shipments).

## Add Shipments To Batch

Adds shipments to an existing batch in EasyPost.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/add-shipments-to-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "shipments[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/add-shipments-to-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "shipments[]": [{}]
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
      "id": "string",
      "labelUrl": "https://example.com",
      "mode": "string",
      "numShipments": 1,
      "object": "string",
      "scanForm": {},
      "shipments": [
        {}
      ],
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Shipments To Batch action reference](actions/add-shipments-to-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyPost/latest/actions/add-shipments-to-batch).

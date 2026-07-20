# Cartloom Universal API Examples

These examples use the MindCloud API key and Cartloom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Discount

Retrieves a discount record from Cartloom by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/get-discount?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/get-discount?${params}`, {
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
      "allowance": "string",
      "amount": "string",
      "auto": "string",
      "code": "string",
      "enabled": "string",
      "id": "string",
      "sid": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "stopDate": "2026-05-07T12:00:00.000Z",
      "target": "string",
      "type": "string",
      "used": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Discount action reference](actions/get-discount.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cartloom/latest/actions/get-discount).

## Add Discount

Creates a new discount in Cartloom.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/add-discount" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "enabled": "1",
  "auto": "0",
  "type": "fixed",
  "unlimited": "0",
  "amount": 1,
  "target": "all",
  "startDate": "2026-05-07T12:00:00.000Z",
  "stopDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/add-discount', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "enabled": "1",
    "auto": "0",
    "type": "fixed",
    "unlimited": "0",
    "amount": 1,
    "target": "all",
    "startDate": "2026-05-07T12:00:00.000Z",
    "stopDate": "2026-05-07T12:00:00.000Z"
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
      "id": 1,
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Discount action reference](actions/add-discount.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cartloom/latest/actions/add-discount).

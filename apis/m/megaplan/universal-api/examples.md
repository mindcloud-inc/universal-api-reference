# Megaplan Universal API Examples

These examples use the MindCloud API key and Megaplan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Account Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/get-account-info?${params}`, {
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
      "contentType": "string",
      "data": {},
      "id": "string",
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/megaplan/latest/actions/get-account-info).

## Create Consignment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/p-ost-consignment-ide28969a6" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/p-ost-consignment-ide28969a6', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "id": 1,
    "body": {}
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
      "contentType": "string",
      "data": {},
      "id": "string",
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Consignment action reference](actions/p-ost-consignment-ide28969a6.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/megaplan/latest/actions/p-ost-consignment-ide28969a6).

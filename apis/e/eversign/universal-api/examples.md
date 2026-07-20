# Eversign Universal API Examples

These examples use the MindCloud API key and Eversign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Businesses

Retrieves business records from your Eversign account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eversign/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eversign/latest/actions/list-businesses?${params}`, {
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
      "business_connection_id": "string",
      "business_id": 1,
      "business_identifier": "string",
      "business_name": "Ava Chen",
      "business_status": 1,
      "creation_time_stamp": 1,
      "is_primary": 1
    }
  ],
  "meta": {}
}
```

See the full [List Businesses action reference](actions/list-businesses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eversign/latest/actions/list-businesses).

## Cancel Document

Cancels an existing document in Eversign.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eversign/latest/actions/cancel-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentHash": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eversign/latest/actions/cancel-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentHash": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Cancel Document action reference](actions/cancel-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eversign/latest/actions/cancel-document).

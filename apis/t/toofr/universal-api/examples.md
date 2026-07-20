# Toofr Universal API Examples

These examples use the MindCloud API key and Toofr connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Domain

Retrieves a company's domain from Toofr.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-company-domain?connectionId=$CONNECTION_ID&companyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-company-domain?${params}`, {
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
      "domain": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company Domain action reference](actions/get-company-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/toofr/latest/actions/get-company-domain).

## Bulk Create Email List Records

Creates multiple email list records in Toofr.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/bulk-create-email-list-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "records": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toofr/latest/actions/bulk-create-email-list-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "records": "string"
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
      "created": 1,
      "errors": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Bulk Create Email List Records action reference](actions/bulk-create-email-list-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/toofr/latest/actions/bulk-create-email-list-records).

# Direct Mail Manager Universal API Examples

These examples use the MindCloud API key and Direct Mail Manager connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Mailing Lists



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-mailing-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-mailing-lists?${params}`, {
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
      "addresses_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "locked_at": "2026-05-07T12:00:00.000Z",
      "mailable_count": 1,
      "name": "Ava Chen",
      "object": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Mailing Lists action reference](actions/list-mailing-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/directMailManager/latest/actions/list-mailing-lists).

## Attach Address To Mailing List



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/attach-address-to-mailing-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/attach-address-to-mailing-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "address_city": "string",
      "address_country": "string",
      "address_line1": "string",
      "address_line2": "string",
      "address_state": "string",
      "address_zip": "string",
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "first_name": "Ava",
      "id": "string",
      "is_deliverable": true,
      "last_name": "Chen",
      "object": "string",
      "suppressed_at": "2026-05-07T12:00:00.000Z",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "verification_status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Attach Address To Mailing List action reference](actions/attach-address-to-mailing-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/directMailManager/latest/actions/attach-address-to-mailing-list).

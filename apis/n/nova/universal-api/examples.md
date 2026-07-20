# Nova Universal API Examples

These examples use the MindCloud API key and Nova connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated Company



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nova/latest/actions/get-authenticated-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nova/latest/actions/get-authenticated-company?${params}`, {
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
      "company_id": 1,
      "company_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated Company action reference](actions/get-authenticated-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nova/latest/actions/get-authenticated-company).

## Add Lead



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nova/latest/actions/add-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": "28",
  "phone_number_concatenated": "+33777777777"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nova/latest/actions/add-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": "28",
    "phone_number_concatenated": "+33777777777"
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
      "access_id": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "lastname": "Chen",
      "list_id": 1,
      "phone_number_concatenated": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Lead action reference](actions/add-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nova/latest/actions/add-lead).

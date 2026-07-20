# Envoice Universal API Examples

These examples use the MindCloud API key and Envoice connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Countries

Retrieves supported countries from Envoice.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-countries?${params}`, {
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
      "Id": 1,
      "Name": "Ava Chen",
      "Value": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Countries action reference](actions/list-countries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/envoice/latest/actions/list-countries).

## Change Estimation Status

Updates an estimation status in Envoice.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-estimation-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-estimation-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "status": "string"
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
      "Success": true
    }
  ],
  "meta": {}
}
```

See the full [Change Estimation Status action reference](actions/change-estimation-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/envoice/latest/actions/change-estimation-status).

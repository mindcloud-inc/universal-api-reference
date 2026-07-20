# Knack Universal API Examples

These examples use the MindCloud API key and Knack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Records



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/knack/latest/actions/list-records?connectionId=$CONNECTION_ID&objectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/knack/latest/actions/list-records?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Records action reference](actions/list-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/knack/latest/actions/list-records).

## Create Record



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/knack/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/knack/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectKey": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Record action reference](actions/create-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/knack/latest/actions/create-record).

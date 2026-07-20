# Beebole Universal API Examples

These examples use the MindCloud API key and Beebole connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Companies

Retrieves companies from your Beebole account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beebole/latest/actions/list-companies?${params}`, {
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

See the full [List Companies action reference](actions/list-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beebole/latest/actions/list-companies).

## Activate a Company

Activates a company in Beebole.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/activate-a-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beebole/latest/actions/activate-a-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
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

See the full [Activate a Company action reference](actions/activate-a-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beebole/latest/actions/activate-a-company).

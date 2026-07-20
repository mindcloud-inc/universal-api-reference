# Apiary Universal API Examples

These examples use the MindCloud API key and Apiary connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List APIs

Finds APIs in your Apiary account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apiary/latest/actions/list-ap-is?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apiary/latest/actions/list-ap-is?${params}`, {
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

See the full [List APIs action reference](actions/list-ap-is.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apiary/latest/actions/list-ap-is).

## Publish Blueprint

Publishes an API blueprint in Apiary.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apiary/latest/actions/publish-blueprint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apiName": "mindcloudapp",
  "code": "string",
  "shouldCommit": "no"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apiary/latest/actions/publish-blueprint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apiName": "mindcloudapp",
    "code": "string",
    "shouldCommit": "no"
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

See the full [Publish Blueprint action reference](actions/publish-blueprint.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apiary/latest/actions/publish-blueprint).

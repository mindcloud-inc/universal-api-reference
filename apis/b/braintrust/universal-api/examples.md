# Braintrust Universal API Examples

These examples use the MindCloud API key and Braintrust connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from Braintrust.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/list-organizations?${params}`, {
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
      "apiUrl": {},
      "created": "string",
      "id": "string",
      "imageRenderingMode": {},
      "isDataplanePrivate": {},
      "isUniversalApi": {},
      "name": "Ava Chen",
      "proxyUrl": {},
      "realtimeUrl": {}
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/braintrust/latest/actions/list-organizations).

## Create Dataset

Creates a new dataset in Braintrust.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/create-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/create-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "name": "Ava Chen"
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

See the full [Create Dataset action reference](actions/create-dataset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/braintrust/latest/actions/create-dataset).

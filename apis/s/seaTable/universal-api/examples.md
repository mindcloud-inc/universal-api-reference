# SeaTable Universal API Examples

These examples use the MindCloud API key and SeaTable connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Base Token With API Token

Retrieves a SeaTable base token with an API token.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-base-token-with-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-base-token-with-api-token?${params}`, {
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
      "accessToken": "string",
      "appName": "Ava Chen",
      "dtableName": "Ava Chen",
      "dtableServer": "string",
      "dtableUuid": "string",
      "useApiGateway": true,
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Base Token With API Token action reference](actions/get-base-token-with-api-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seaTable/latest/actions/get-base-token-with-api-token).

## Add Rows Into Big Data Backend

Adds rows to a SeaTable big data backend.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/add-rows-into-big-data-backend" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/add-rows-into-big-data-backend', {
  method: 'POST',
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
      "insertedRowCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Rows Into Big Data Backend action reference](actions/add-rows-into-big-data-backend.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seaTable/latest/actions/add-rows-into-big-data-backend).

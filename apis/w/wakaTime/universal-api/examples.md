# WakaTime Universal API Examples

These examples use the MindCloud API key and WakaTime connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current WakaTime user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/get-current-user?${params}`, {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wakaTime/latest/actions/get-current-user).

## Create Current Data Dump

Creates a WakaTime data export.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/create-current-data-dump" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/create-current-data-dump', {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Current Data Dump action reference](actions/create-current-data-dump.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wakaTime/latest/actions/create-current-data-dump).

# HiDrive Universal API Examples

These examples use the MindCloud API key and HiDrive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get App Info

Retrieves app information from HiDrive.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-app-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-app-info?${params}`, {
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
      "created": 1,
      "developer": {},
      "homepage": "string",
      "id": 1,
      "name": "Ava Chen",
      "refresh_token": {
        "scope": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get App Info action reference](actions/get-app-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hidrive/latest/actions/get-app-info).

## Copy Directory

Copies a directory in HiDrive.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/copy-directory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dst": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/copy-directory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dst": "string"
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
      "ctime": 1,
      "id": "string",
      "mtime": 1,
      "name": "Ava Chen",
      "parent_id": "string",
      "path": "string",
      "readable": true,
      "type": "string",
      "writable": true
    }
  ],
  "meta": {}
}
```

See the full [Copy Directory action reference](actions/copy-directory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hidrive/latest/actions/copy-directory).

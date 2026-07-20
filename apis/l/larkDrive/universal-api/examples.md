# Lark Drive Universal API Examples

These examples use the MindCloud API key and Lark Drive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check File Task



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/check-file-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/check-file-task?${params}`, {
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
      "code": 1,
      "data": {
        "status": "string"
      },
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check File Task action reference](actions/check-file-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/larkDrive/latest/actions/check-file-task).

## Copy File



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/copy-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileToken": "string",
  "name": "Ava Chen",
  "folderToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/copy-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileToken": "string",
    "name": "Ava Chen",
    "folderToken": "string"
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
      "code": 1,
      "data": {
        "file": {
          "name": "Ava Chen",
          "parent_token": "string",
          "token": "string",
          "type": "string",
          "url": "https://example.com"
        }
      },
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Copy File action reference](actions/copy-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/larkDrive/latest/actions/copy-file).

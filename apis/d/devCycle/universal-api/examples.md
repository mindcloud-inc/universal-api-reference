# DevCycle Universal API Examples

These examples use the MindCloud API key and DevCycle connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Environments

Retrieves environments from DevCycle.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-environments?connectionId=$CONNECTION_ID&limit=25&offset=0&project=mindcloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "project": "mindcloud"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-environments?${params}`, {
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
      "color": "string",
      "createdAt": "string",
      "createdBy": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "readonly": true,
      "sdkKeys": {
        "client": [
          [
            {}
          ]
        ],
        "mobile": [
          [
            {}
          ]
        ],
        "server": [
          [
            {}
          ]
        ]
      },
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Environments action reference](actions/list-environments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/devCycle/latest/actions/list-environments).

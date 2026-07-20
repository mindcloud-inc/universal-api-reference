# YepCode Universal API Examples

These examples use the MindCloud API key and YepCode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get processes

Retrieves a list of processes from YepCode.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-processes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-processes?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "parametersSchema": {
        "description": "string",
        "title": "string",
        "type": "string"
      },
      "programmingLanguage": "string",
      "readme": "string",
      "settings": {
        "dependencies": {
          "autoDetect": true,
          "scopedToProcess": true
        },
        "formsConfig": {
          "enabled": true
        },
        "publicConfig": {
          "enabled": true
        }
      },
      "slug": "string",
      "sourceCode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "webhook": {
        "enabled": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Get processes action reference](actions/get-processes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yepCode/latest/actions/get-processes).

## Create module

Creates a new module in YepCode.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-module" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "programmingLanguage": "string",
  "sourceCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-module', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "programmingLanguage": "string",
    "sourceCode": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "id": "string",
      "name": "Ava Chen",
      "programmingLanguage": "string",
      "sourceCode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create module action reference](actions/create-module.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yepCode/latest/actions/create-module).

# Stack AI Universal API Examples

These examples use the MindCloud API key and Stack AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Personal Folder



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-user-personal-folder?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-user-personal-folder?${params}`, {
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
      "access": [
        "string"
      ],
      "group_id_access_list": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "personal_folder_owner_id": "string",
      "user_id_access_list": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get User Personal Folder action reference](actions/get-user-personal-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stackAI/latest/actions/get-user-personal-folder).

## Create Custom Tool



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-custom-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-custom-tool', {
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
      "actions": [
        {}
      ],
      "color": "string",
      "connections": {},
      "deprecation_info": {},
      "description": "string",
      "headers": {},
      "icon": "string",
      "name": "Ava Chen",
      "openapi_schema": "string",
      "provider_group": [
        "string"
      ],
      "provider_id": "string",
      "provider_version": "string",
      "tags": [
        "string"
      ],
      "triggers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Custom Tool action reference](actions/create-custom-tool.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stackAI/latest/actions/create-custom-tool).

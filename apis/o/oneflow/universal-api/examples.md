# Oneflow Universal API Examples

These examples use the MindCloud API key and Oneflow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces from Oneflow.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-workspaces?${params}`, {
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
      "_integration_permissions": [
        {}
      ],
      "_links": {},
      "_permissions": {},
      "company_name": "Ava Chen",
      "country_code": "string",
      "created_time": "string",
      "date_format": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "registration_number": "string",
      "type": "string",
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneflow/latest/actions/list-workspaces).

## Create Access Link

Creates an access link in Oneflow.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-access-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractId": "string",
  "participantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-access-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contractId": "string",
    "participantId": "string"
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
      "access_link": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Access Link action reference](actions/create-access-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneflow/latest/actions/create-access-link).

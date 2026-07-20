# openpm Universal API Examples

These examples use the MindCloud API key and openpm connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Packages



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openpm/latest/actions/list-packages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openpm/latest/actions/list-packages?${params}`, {
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
      "contact_email": "ava@example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domain": "string",
      "id": "string",
      "legal_info_url": "https://example.com",
      "logo_url": "https://example.com",
      "machine_description": "string",
      "machine_name": "Ava Chen",
      "name": "Ava Chen",
      "published_at": "2026-05-07T12:00:00.000Z",
      "total_count": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Packages action reference](actions/list-packages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openpm/latest/actions/list-packages).

## Create Package



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openpm/latest/actions/create-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "openapi": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openpm/latest/actions/create-package', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "openapi": "string"
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
      "id": "string",
      "openapi": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Package action reference](actions/create-package.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openpm/latest/actions/create-package).

# Ninetailed Universal API Examples

These examples use the MindCloud API key and Ninetailed connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organization Spaces



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/list-organization-spaces?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/list-organization-spaces?${params}`, {
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
      "name": "Ava Chen",
      "sys": {}
    }
  ],
  "meta": {}
}
```

See the full [List Organization Spaces action reference](actions/list-organization-spaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ninetailed/latest/actions/list-organization-spaces).

## Activate Content Type



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/activate-content-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "environmentId": "string",
  "contentTypeId": "string",
  "contentfulVersion": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/activate-content-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "environmentId": "string",
    "contentTypeId": "string",
    "contentfulVersion": 1
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
      "description": "string",
      "displayField": "string",
      "fields": [
        {}
      ],
      "name": "Ava Chen",
      "sys": {}
    }
  ],
  "meta": {}
}
```

See the full [Activate Content Type action reference](actions/activate-content-type.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ninetailed/latest/actions/activate-content-type).

# Zoho Recruit Universal API Examples

These examples use the MindCloud API key and Zoho Recruit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Modules

Retrieves all modules from Zoho Recruit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-modules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-modules?${params}`, {
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
      "apiName": "Ava Chen",
      "apiSupported": true,
      "creatable": true,
      "deletable": true,
      "displayField": {},
      "editable": true,
      "filterSupported": true,
      "id": "string",
      "moduleName": "Ava Chen",
      "parentModule": {},
      "pluralLabel": "string",
      "profiles": [
        {}
      ],
      "singularLabel": "string",
      "viewable": true
    }
  ],
  "meta": {}
}
```

See the full [List Modules action reference](actions/list-modules.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoRecruit/latest/actions/list-modules).

## Add Tags

Adds tags to a Zoho Recruit record.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/add-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleApiName": "Ava Chen",
  "recordId": "string",
  "tagNames": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/add-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleApiName": "Ava Chen",
    "recordId": "string",
    "tagNames": "Ava Chen"
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
      "code": "string",
      "details": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Tags action reference](actions/add-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoRecruit/latest/actions/add-tags).

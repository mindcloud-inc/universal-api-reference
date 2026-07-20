# Templated Universal API Examples

These examples use the MindCloud API key and Templated connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information

Retrieves detailed account information from Templated.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templated/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templated/latest/actions/get-account-information?${params}`, {
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
      "apiQuota": 1,
      "apiUsage": 1,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "plan": "string",
      "teamName": "Ava Chen",
      "usagePercentage": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/templated/latest/actions/get-account-information).

## Clone Template

Clones an existing template in Templated.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/templated/latest/actions/clone-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/templated/latest/actions/clone-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
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
      "categoryId": "string",
      "categoryName": "Ava Chen",
      "createdAt": "string",
      "description": "string",
      "duration": 1,
      "externalId": "string",
      "folderId": "string",
      "folderName": "Ava Chen",
      "height": 1,
      "html": "string",
      "id": "string",
      "isClone": true,
      "isMaster": true,
      "layersCount": 1,
      "multiSizePages": true,
      "name": "Ava Chen",
      "pagesCount": 1,
      "ranking": 1,
      "removed": true,
      "sourceTemplateId": "string",
      "sourceTemplateName": "Ava Chen",
      "tags": [
        "string"
      ],
      "teamId": "string",
      "thumbnail": "string",
      "type": "string",
      "updatedAt": "string",
      "userId": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [Clone Template action reference](actions/clone-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/templated/latest/actions/clone-template).

# Gupshup Universal API Examples

These examples use the MindCloud API key and Gupshup connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Templates For App

Retrieves all templates for a Gupshup app.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-all-templates-for-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-all-templates-for-app?${params}`, {
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
      "pageNo": 1,
      "pageSize": 1,
      "templates": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [Get All Templates For App action reference](actions/get-all-templates-for-app.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gupshup/latest/actions/get-all-templates-for-app).

## Create Template

Creates a template in Gupshup.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "languageCode": "string",
  "content": "string",
  "category": "string",
  "elementName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "languageCode": "string",
    "content": "string",
    "category": "string",
    "elementName": "Ava Chen"
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
      "message": "string",
      "status": "string",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Template action reference](actions/create-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gupshup/latest/actions/create-template).

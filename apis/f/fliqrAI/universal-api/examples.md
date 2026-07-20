# Fliqr AI Universal API Examples

These examples use the MindCloud API key and Fliqr AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Business Account Details

Retrieves business account details from Fliqr AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/get-business-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/get-business-account-details?${params}`, {
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
      "active": true,
      "created": "string",
      "name": "Ava Chen",
      "pageId": "string",
      "totalUsers": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Business Account Details action reference](actions/get-business-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fliqrAI/latest/actions/get-business-account-details).

## Add Tag To Contact

Creates a tag assignment for a contact in Fliqr AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/add-tag-to-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1,
  "tagId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/add-tag-to-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1,
    "tagId": 1
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Tag To Contact action reference](actions/add-tag-to-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fliqrAI/latest/actions/add-tag-to-contact).

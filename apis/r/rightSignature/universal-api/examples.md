# RightSignature Universal API Examples

These examples use the MindCloud API key and RightSignature connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Me

Retrieves the authenticated RightSignature user profile.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-me?${params}`, {
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
      "avatarUrl": "https://example.com",
      "cancellationDate": "string",
      "canSendDocuments": true,
      "company": "string",
      "email": "ava@example.com",
      "id": "string",
      "isGracePeriod": true,
      "name": "Ava Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Me action reference](actions/get-me.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rightSignature/latest/actions/get-me).

## Add Or Update Reusable Template Tags

Adds or updates tags on a RightSignature reusable template.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/add-or-update-reusable-template-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tags": {},
  "tags.tagName": "Ava Chen",
  "reusableTemplateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/add-or-update-reusable-template-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tags": {},
    "tags.tagName": "Ava Chen",
    "reusableTemplateId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Or Update Reusable Template Tags action reference](actions/add-or-update-reusable-template-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rightSignature/latest/actions/add-or-update-reusable-template-tags).

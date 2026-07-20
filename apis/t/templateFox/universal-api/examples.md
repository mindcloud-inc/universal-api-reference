# TemplateFox Universal API Examples

These examples use the MindCloud API key and TemplateFox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from TemplateFox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/get-account?${params}`, {
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
      "credits": 1,
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/templateFox/latest/actions/get-account).

## Create PDF

Creates a PDF from a template in TemplateFox.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/create-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "HMQywVpZxqAM",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/create-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "HMQywVpZxqAM",
    "data": "[object Object]"
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
      "credits_remaining": 1,
      "expires_in": 1,
      "filename": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create PDF action reference](actions/create-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/templateFox/latest/actions/create-pdf).

# CraftMyPDF Universal API Examples

These examples use the MindCloud API key and CraftMyPDF connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get account information

Retrieves account information from your CraftMyPDF account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-account-information?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "isTeam": true,
      "quotaCounter": 1,
      "quotaMax": 1,
      "status": "string",
      "templateCounter": 1,
      "templateMax": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get account information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/craftMyPDF/latest/actions/get-account-information).

## Add text to a PDF

Adds text to a PDF in CraftMyPDF.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/add-text-to-apdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "textSettings[]": [
    {}
  ],
  "textSettings[].pageSelector": "string",
  "textSettings[].text": "string",
  "textSettings[].position": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/add-text-to-apdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "textSettings[]": [{}],
    "textSettings[].pageSelector": "string",
    "textSettings[].text": "string",
    "textSettings[].position": "string"
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
      "file": "string",
      "status": "string",
      "transactionRef": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add text to a PDF action reference](actions/add-text-to-apdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/craftMyPDF/latest/actions/add-text-to-apdf).

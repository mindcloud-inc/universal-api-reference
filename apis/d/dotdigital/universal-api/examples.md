# Dotdigital Universal API Examples

These examples use the MindCloud API key and Dotdigital connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information

Retrieves account status information from Dotdigital.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-account-information?${params}`, {
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
      "id": 1,
      "properties": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dotdigital/latest/actions/get-account-information).

## Create Campaign

Creates a new campaign in Dotdigital.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "subject": "string",
  "fromName": "Ava Chen",
  "htmlContent": "string",
  "plainTextContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "subject": "string",
    "fromName": "Ava Chen",
    "htmlContent": "string",
    "plainTextContent": "string"
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
      "customReplyToAddress": "string",
      "fromAddress": {
        "email": "ava@example.com",
        "id": 1
      },
      "fromName": "Ava Chen",
      "htmlContent": "string",
      "id": 1,
      "isSplitTest": true,
      "name": "Ava Chen",
      "plainTextContent": "string",
      "replyAction": "string",
      "replyToAddress": "string",
      "status": "string",
      "subject": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Campaign action reference](actions/create-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dotdigital/latest/actions/create-campaign).

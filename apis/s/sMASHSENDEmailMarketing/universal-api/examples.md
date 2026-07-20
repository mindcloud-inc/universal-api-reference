# SMASHSEND Email Marketing Universal API Examples

These examples use the MindCloud API key and SMASHSEND Email Marketing connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate API Key

Validates a SMASHSEND API key and returns its details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/validate-api-key?${params}`, {
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
      "displayName": "Ava Chen",
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate API Key action reference](actions/validate-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMASHSENDEmailMarketing/latest/actions/validate-api-key).

## Create Contact Property

Creates a new contact property in SMASHSEND.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/create-contact-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/create-contact-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Ava Chen",
    "type": "string"
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

See the full [Create Contact Property action reference](actions/create-contact-property.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMASHSENDEmailMarketing/latest/actions/create-contact-property).

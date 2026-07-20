# Stripo Universal API Examples

These examples use the MindCloud API key and Stripo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Token

Validates a Stripo API token.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/validate-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/validate-token?${params}`, {
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
      "protocolVersion": "string",
      "valid": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Token action reference](actions/validate-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stripo/latest/actions/validate-token).

## Apply Email Translations JSON

Applies email translations from a JSON file in Stripo.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/apply-email-translations-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "id": 1,
  "targetLanguages[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripo/latest/actions/apply-email-translations-json', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "id": 1,
    "targetLanguages[]": ["string"]
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

See the full [Apply Email Translations JSON action reference](actions/apply-email-translations-json.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stripo/latest/actions/apply-email-translations-json).

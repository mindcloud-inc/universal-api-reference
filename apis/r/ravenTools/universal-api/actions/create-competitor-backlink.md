# Raven Tools: Create Competitor Backlink

Creates a new competitor backlink in Raven Tools.

```
POST https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/create-competitor-backlink
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/create-competitor-backlink" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "link": "JSON array with one competitor backlink Raven link record to create."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/create-competitor-backlink', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "link": "JSON array with one competitor backlink Raven link record to create."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `link` | string | yes | JSON-encoded string for one competitor-backlink Raven link record. Default: `[{"domain":"codex-raven-tools-verify-20260408.example","status":"active","link url":"https://mindcloud.co/competitor","link text":"Competitor Raven Link","link type":"Competitor Backlink","website url":"https://example.com/competitor","website type":"Other"}]`. Example: `JSON array with one competitor backlink Raven link record to create.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number | Created Raven link id. |

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-competitor-backlink.md) for the provider-specific parameters and requirements.


# Wikibot: Create Knowledge Base

Creates a new knowledge base in Wikibot.

```
POST https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/create-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikibot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/create-knowledge-base" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/help"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/create-knowledge-base', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/help"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Source data URL for the knowledge base. Example: `https://example.com/help`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether Wikibot accepted the knowledge base creation request. |

## Native endpoint

Through the native Wikibot API, this operation is `POST /bot/kb/create` (base URL `https://api.wikibot.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-knowledge-base.md) for the provider-specific parameters and requirements.


# WebAutomation.io: Add Starter Links

Replaces an extractor's starter links with a new list.

```
POST https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/add-starter-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebAutomation.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/add-starter-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extractorId": 1,
  "startUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/add-starter-links', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extractorId": 1,
    "startUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extractorId` | number | yes | The extractor ID. |
| `startUrls[]` | array<string> | yes | The list of start URLs to set on the extractor. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebAutomation.io API returns.

## Native endpoint

Through the native WebAutomation.io API, this operation is `POST /extractors/start_urls/{{EXTRACTOR_ID}}/` (base URL `https://webautomation.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-starter-links.md) for the provider-specific parameters and requirements.


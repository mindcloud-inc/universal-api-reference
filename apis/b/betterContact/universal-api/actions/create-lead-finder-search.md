# BetterContact: Create Lead Finder Search

Creates an asynchronous BetterContact lead finder search.

```
POST https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/create-lead-finder-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BetterContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/create-lead-finder-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filters": "[object Object]",
  "maxLeads": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/create-lead-finder-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filters": "[object Object]",
    "maxLeads": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | object | yes | Lead finder filters object, for example {"company":{"include":["OpenAI"]},"lead_seniority":{"include":["founder"]}}. Example: `[object Object]`. |
| `maxLeads` | number | yes | Maximum number of leads to return. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "requestId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `requestId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native BetterContact API, this operation is `POST /lead_finder/async` (base URL `https://app.bettercontact.rocks/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead-finder-search.md) for the provider-specific parameters and requirements.


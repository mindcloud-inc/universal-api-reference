# Cloutly: Create Business

Creates a new business in Cloutly.

```
POST https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/create-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloutly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/create-business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/create-business', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Business name to create in Cloutly marketplace. |
| `senderName` | string | no | External-friendly display label for the business. |
| `address` | string | no | Business address. |
| `industry` | string | no | Business industry. |
| `website` | string | no | Business website URL or hostname. |
| `logoUrl` | string | no | Hosted logo URL for the business. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `googlePlaceId` | string | no | Google Place ID to connect Google review sources. |
| `facebookUrl` | string | no | Facebook page URL to connect Facebook review sources. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloutly API returns.

## Native endpoint

Through the native Cloutly API, this operation is `POST https://marketplace.cloutly.com/api/v2/businesses` (base URL `https://app.cloutly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-business.md) for the provider-specific parameters and requirements.


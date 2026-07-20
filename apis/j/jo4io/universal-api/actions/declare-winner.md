# jo4.io: Declare A/B Test Winner



```
PUT https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/declare-winner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/declare-winner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string",
  "variantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/declare-winner', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string",
    "variantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | yes |  |
| `variantId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native jo4.io API returns.

## Native endpoint

Through the native jo4.io API, this operation is `POST /protected/url/:slug/ab-test/winner/:variantId` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/declare-winner.md) for the provider-specific parameters and requirements.


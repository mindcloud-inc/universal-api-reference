# iLoveSign: Increase Expiration Days



```
PUT https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/increase-expiration-days
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLoveSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/increase-expiration-days" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tokenRequester": "string",
  "days": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/increase-expiration-days', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tokenRequester": "string",
    "days": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tokenRequester` | string | yes | Signature request token requester identifier. |
| `days` | number | yes | Number of additional days to add, between 1 and 130. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iLoveSign API returns.

## Native endpoint

Through the native iLoveSign API, this operation is `PUT /signature/increase-expiration-days/:token_requester` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/increase-expiration-days.md) for the provider-specific parameters and requirements.


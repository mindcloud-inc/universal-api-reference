# eBay: Opt-In to Program

This method opts the seller in to an eBay seller program. Refer to the Account API overview for information about available eBay seller programs.

```
PUT https://connect.mindcloud.co/v1/universal/ebay/latest/actions/opt-in-to-program
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/opt-in-to-program" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ebay/latest/actions/opt-in-to-program', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `programType` | list<string> | no | The Seller Program to opt-in to. One of: `OUT_OF_STOCK_CONTROL`, `PARTNER_MOTORS_DEALER`, `SELLING_POLICY_MANAGEMENT`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eBay API returns.

## Native endpoint

Through the native eBay API, this operation is `POST sell/account/v1/program/opt_in` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/opt-in-to-program.md) for the provider-specific parameters and requirements.


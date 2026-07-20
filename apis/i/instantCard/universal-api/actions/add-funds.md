# InstantCard: Add Funds

Adds funds to an InstantCard organization balance.

```
POST https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/add-funds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/add-funds" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "20003827",
  "amount": "1.00",
  "number": "4242424242424242",
  "expMonth": "06",
  "expYear": "2029",
  "cvc": "424",
  "fullName": "InstantCard API",
  "billingAddress1": "418 Highland Rd.",
  "billingCountry": "USA",
  "billingCity": "Feasterville",
  "billingState": "PA",
  "billingZipCode": "19053"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/add-funds', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "20003827",
    "amount": "1.00",
    "number": "4242424242424242",
    "expMonth": "06",
    "expYear": "2029",
    "cvc": "424",
    "fullName": "InstantCard API",
    "billingAddress1": "418 Highland Rd.",
    "billingCountry": "USA",
    "billingCity": "Feasterville",
    "billingState": "PA",
    "billingZipCode": "19053"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAddress2` | string | no | Billing address line 2. |
| `channel` | string | no | Payment channel. |
| `organizationId` | number | yes | Organization ID from InstantCard. Example: `20003827`. |
| `amount` | string | yes | Amount to add. Example: `1.00`. |
| `number` | string | yes | Credit card number. Example: `4242424242424242`. |
| `expMonth` | string | yes | Card expiration month. Example: `06`. |
| `expYear` | string | yes | Card expiration year. Example: `2029`. |
| `cvc` | string | yes | Card security code. Example: `424`. |
| `fullName` | string | yes | Cardholder full name. Example: `InstantCard API`. |
| `billingAddress1` | string | yes | Billing address line 1. Example: `418 Highland Rd.`. |
| `billingCountry` | string | yes | Billing country. Example: `USA`. |
| `billingCity` | string | yes | Billing city. Example: `Feasterville`. |
| `billingState` | string | yes | Billing state. Example: `PA`. |
| `billingZipCode` | string | yes | Billing postal code. Example: `19053`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native InstantCard API returns.

## Native endpoint

Through the native InstantCard API, this operation is `POST /api/v2/organizations/:organizationId/add_funds` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-funds.md) for the provider-specific parameters and requirements.


# Outseta: Add Account with Subscription

Creates an account with a subscription in Outseta.

```
POST https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-account-with-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-account-with-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-account-with-subscription', {
  method: 'POST',
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
| `name` | string | no |  |
| `mailingAddress.addressLine1` | string | no |  |
| `mailingAddress.addressLine2` | string | no |  |
| `mailingAddress.city` | string | no |  |
| `mailingAddress.state` | string | no |  |
| `mailingAddress.postalCode` | string | no |  |
| `billingAddress.addressLine1` | string | no |  |
| `billingAddress.addressLine2` | string | no |  |
| `billingAddress.city` | string | no |  |
| `billingAddress.state` | string | no |  |
| `billingAddress.postalCode` | string | no |  |
| `personAccount[].person.uid` | string | no |  |
| `personAccount[].isPrimary` | string | no |  |
| `subscriptions[].plan.uid` | string | no |  |
| `subscriptions[].billingRenewalTerm` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AccountStage": 1,
      "ClientIdentifier": "string",
      "Created": "string",
      "Name": "Ava Chen",
      "Uid": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountStage` | number |  |
| `ClientIdentifier` | string |  |
| `Created` | string |  |
| `Name` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `POST /crm/accounts` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-account-with-subscription.md) for the provider-specific parameters and requirements.


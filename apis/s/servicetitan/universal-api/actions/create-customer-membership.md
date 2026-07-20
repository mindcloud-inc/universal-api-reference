# ServiceTitan: Create Customer Membership

Creates a customer membership sale in ServiceTitan.

```
POST https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-customer-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-customer-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "businessUnitId": 1,
  "saleTaskId": 1,
  "durationBillingId": 1,
  "recurringServiceAction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-customer-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "businessUnitId": 1,
    "saleTaskId": 1,
    "durationBillingId": 1,
    "recurringServiceAction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | ID of the customer you are creating the Membership Sale Invoice for |
| `businessUnitId` | number | yes | Business unit ID |
| `saleTaskId` | number | yes | ID of the sale task that is creating the membership |
| `durationBillingId` | number | yes | ID of the duration/billing option to be used |
| `locationId` | number | no |  |
| `recurringServiceAction` | string | yes | Required if RecurringLocationId is set. Determines how many of the customer's locations that recurring services should be added to: all, single, or none (which deletes existing recurring services). |
| `recurringLocationId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerMembershipId": 1,
      "Invoice ID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerMembershipId` | number |  |
| `Invoice ID` | number |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `POST memberships/v2/tenant/{{credentials.tenant}}/memberships/sale` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-membership.md) for the provider-specific parameters and requirements.


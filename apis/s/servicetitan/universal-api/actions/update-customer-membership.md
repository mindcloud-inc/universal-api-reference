# ServiceTitan: Update Customer Membership

Updates an existing customer membership in ServiceTitan.

```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-customer-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-customer-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-customer-membership', {
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
| `membershipId` | number | no |  |
| `businessUnitId` | number | no | Business unit ID |
| `nextScheduledBillDate` | string | no | Next date that this membership will be billed on |
| `status` | list | no |  |
| `memo` | string | no |  |
| `from` | date | no |  |
| `to` | date | no | The end date of this membership (null if ongoing) |
| `billingTemplateId` | number | no | The ID of the invoice template used to bill this membership. Can either be a "settings template" (when invoice template is shared – in this case new invoice template will be created), or be a new invoice template created specifically for this customer membership. |
| `soldByID` | number | no | ID of the user that was credited for the sale of this membership |
| `locationId` | number | no |  |
| `recurringServiceAction` | string | no | Required if RecurringLocationId is set. Determines how many of the customer's locations that recurring services should be added to: all, single, or none (which deletes existing recurring services). |
| `recurringLocationId` | number | no |  |
| `cancellationBalanceInvoiceId` | number | no |  |
| `cancellationInvoiceId` | number | no |  |
| `initialDeferredRevenue` | number | no |  |
| `paymentMethodId` | number | no |  |
| `paymentTypeId` | number | no |  |
| `renewalMembershipTaskId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | number |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `PATCH memberships/v2/tenant/{{credentials.tenant}}/memberships/:membershipId` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer-membership.md) for the provider-specific parameters and requirements.


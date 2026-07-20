# Aspire: Create Opportunity

Updates an existing pay code in your Aspire account.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-new-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-new-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "opportunityType": "Contract",
  "opportunityName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-new-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "opportunityType": "Contract",
    "opportunityName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opportunityType` | list<string> | yes | One of: `Contract`, `Work Order`. Default: `Contract`. |
| `opportunityName` | string | yes |  |
| `invoiceType` | string | no |  |
| `opportunityTags` | string | no |  |
| `customerContractNum` | string | no |  |
| `customerPONum` | string | no |  |
| `salesRepContactName` | string | no |  |
| `branchID` | list<number> | no |  |
| `templateOpportunityID` | list<number> | no |  |
| `leadSourceID` | list<number> | no |  |
| `salesRepID` | list<number> | no |  |
| `salesTypeID` | list<number> | no |  |
| `masterOpportunityID` | list<number> | no |  |
| `division` | list<number> | no |  |
| `property` | list<number> | no |  |
| `operationsMgrID` | list<number> | no |  |
| `bidDueDate` | date | no |  |
| `renewalDate` | date | no |  |
| `anticipatedCloseDate` | date | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `probability` | number | no |  |
| `budgetedDollars` | number | no |  |
| `estimatedDollars` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "opportunityID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `opportunityID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `POST Opportunities` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-opportunity.md) for the provider-specific parameters and requirements.


# Autotask: Create Opportunity



```
POST https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autotask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "companyID": 1,
  "cost": 1,
  "ownerResourceID": 1,
  "probability": 1,
  "projectedCloseDate": "2026-05-07T12:00:00.000Z",
  "stage": 1,
  "startDate": "2026-05-07T12:00:00.000Z",
  "status": 1,
  "title": "string",
  "useQuoteTotals": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "companyID": 1,
    "cost": 1,
    "ownerResourceID": 1,
    "probability": 1,
    "projectedCloseDate": "2026-05-07T12:00:00.000Z",
    "stage": 1,
    "startDate": "2026-05-07T12:00:00.000Z",
    "status": 1,
    "title": "string",
    "useQuoteTotals": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes |  |
| `companyID` | number | yes |  |
| `cost` | number | yes |  |
| `ownerResourceID` | number | yes |  |
| `probability` | number | yes |  |
| `projectedCloseDate` | date | yes |  |
| `stage` | number | yes |  |
| `startDate` | date | yes |  |
| `status` | number | yes |  |
| `title` | string | yes |  |
| `useQuoteTotals` | boolean | yes |  |
| `contactID` | number | no |  |
| `description` | string | no |  |
| `opportunityCategoryID` | number | no |  |
| `nextStep` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Autotask API returns.

## Native endpoint

Through the native Autotask API, this operation is `POST /Opportunities` (base URL `https://webservices14.autotask.net/ATServicesRest/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.


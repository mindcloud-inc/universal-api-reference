# Centerpoint: Create Opportunity



```
POST https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | list<string> | yes |  |
| `name` | string | no |  |
| `options.opportunityNTE` | string | no | Overall opportunity NTE (Not to Exceed) is a contractual clause and cost-control mechanism that sets a maximum, capped amount for the overall opportunity. |
| `price` | number | no |  |
| `opportunityType` | string | no |  |
| `workflowType` | string | no |  |
| `description` | string | no |  |
| `type` | list<string> | no |  |
| `propertyID` | string | no |  |
| `billedCompanyID` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `options.notifications` | list<string> | no |  |
| `options.signatureData.isChecked` | boolean | no |  |
| `options.contractorNTE` | string | no | A contractor NTE (Not to Exceed) is a contractual clause and cost-control mechanism that sets a maximum, capped amount a contractor can charge for a project or service. |
| `options.signatureData.name` | string | no |  |
| `options.signatureData.file` | string | no |  |
| `options.signatureData.date` | string | no |  |
| `options.truckID` | string | no |  |
| `options.attachmentID` | string | no |  |
| `options.signatureData.purchaseOrder` | string | no |  |
| `options.signatureData` | object | no |  |
| `dueDate` | string | no |  |
| `forecastedAt` | string | no |  |
| `projectedCloseDate` | string | no |  |
| `options` | object | no |  |
| `custom` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Centerpoint API returns.

## Native endpoint

Through the native Centerpoint API, this operation is `GET opportunities` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-opportunity.md) for the provider-specific parameters and requirements.


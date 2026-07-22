# Viewpoint Spectrum: Create Work Orders



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-work-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-work-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-work-orders', {
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
| `woNumer` | string | no |  |
| `woReferenceCode` | string | no |  |
| `woJobNumber` | string | no |  |
| `woJobDivision` | string | no |  |
| `billCustomerCode` | string | no |  |
| `contractNumber` | string | no |  |
| `customerPONumber` | list | no |  |
| `customerJob` | date | no |  |
| `woPhone1` | string | no |  |
| `woPhone2` | string | no |  |
| `billContract` | number | no |  |
| `zone` | string | no |  |
| `priorityCode` | string | no |  |
| `woCaseType` | string | no |  |
| `priceType` | string | no |  |
| `totalQuoteAmount` | string | no |  |
| `projectedHours` | string | no |  |
| `estArrival` | string | no |  |
| `dispatchStatusCode` | string | no |  |
| `summaryDescription` | string | no |  |
| `orderedDate` | number | no |  |
| `timeEntered` | string | no |  |
| `requestedDate` | string | no |  |
| `estimatedCompleteTime` | number | no |  |
| `scheduledStartDate` | string | no |  |
| `scheduledStartTime` | string | no |  |
| `dateAssigned` | string | no |  |
| `timeAssigned` | string | no |  |
| `arrivalDate` | string | no |  |
| `arrivalTime` | string | no |  |
| `completeDate` | string | no |  |
| `completeTime` | string | no |  |
| `leadSource` | string | no |  |
| `salesPerson` | string | no |  |
| `takenBy` | string | no |  |
| `arTermsCode` | string | no |  |
| `salesTaxCode` | string | no |  |
| `taxableFlag` | string | no |  |
| `glDepartment` | string | no |  |
| `costCenter` | string | no |  |
| `billtoCode` | string | no |  |
| `overrideEroMarkup` | string | no |  |
| `materialPriceLevel` | string | no |  |
| `priceLevel` | string | no |  |
| `markupCode` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/AddARInvoice` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-work-orders.md) for the provider-specific parameters and requirements.


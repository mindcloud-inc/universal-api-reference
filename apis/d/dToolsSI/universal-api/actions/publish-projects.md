# D-Tools SI: Publish Projects



```
POST https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/publish-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D-Tools SI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/publish-projects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "client": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/publish-projects', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "client": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAddress.street1` | string | no |  |
| `contacts[].name` | string<object> | no |  |
| `items[].id` | string | no |  |
| `locations[].id` | string<object> | no |  |
| `siteAddress.street1` | string | no |  |
| `templateName` | string | no |  |
| `billingAddress.street2` | string | no |  |
| `contacts[].email` | string<object> | no |  |
| `items[]` | array<object> | no |  |
| `items[].typeId` | string | no |  |
| `locations[].name` | string<object> | no |  |
| `siteAddress.street2` | string | no |  |
| `billingAddress.city` | string | no |  |
| `contacts[].phone` | string<object> | no |  |
| `items[].componentId` | string | no |  |
| `locations[].description` | string<object> | no |  |
| `packages[]` | array | no |  |
| `siteAddress.city` | string | no |  |
| `billingAddress.state` | string | no |  |
| `items[].manufacturer` | string | no |  |
| `publishedOn` | date | no |  |
| `siteAddress.state` | string | no |  |
| `billingAddress.postalCode` | string | no |  |
| `id` | string | no |  |
| `items[].model` | string | no |  |
| `siteAddress.postalCode` | string | no |  |
| `billingAddress.country` | string | no |  |
| `integrationProjectId` | string | no |  |
| `items[].packageName` | string | no |  |
| `siteAddress.country` | string | no |  |
| `billingAddress.phone` | string | no |  |
| `client` | string | yes |  |
| `items[].unitCost` | number | no |  |
| `siteAddress.phone` | string | no |  |
| `billingAddress.fax` | string | no |  |
| `clientId` | string | no |  |
| `items[].unitPrice` | number | no |  |
| `siteAddress.fax` | string | no |  |
| `integrationClientId` | string | no |  |
| `items[].quantity` | number | no |  |
| `clientNumber` | string | no |  |
| `name` | string | yes |  |
| `number` | string | no |  |
| `quantityBased` | boolean | no |  |
| `progress` | string | no |  |
| `assignedTo` | string | no |  |
| `salesRep` | string | no |  |
| `projectManager` | string | no |  |
| `designer` | string | no |  |
| `revision` | number | no |  |
| `currencyCode` | string | no |  |
| `currencyRate` | number | no |  |
| `cost` | number | no |  |
| `priceWithoutTax` | number | no |  |
| `margin` | number | no |  |
| `markup` | number | no |  |
| `tax` | number | no |  |
| `price` | number | no |  |
| `hours` | number | no |  |
| `budget` | number | no |  |
| `productPriceType` | string | no |  |
| `clientPONumber` | string | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `estimatedCloseDate` | date | no |  |
| `closeDate` | date | no |  |
| `accountingEstimateNumbers` | string | no |  |
| `scopeOfWork` | string | no |  |
| `notes` | string | no |  |
| `siteAddress` | object | no |  |
| `billingAddress` | object | no |  |
| `isItemLevelTax` | boolean | no |  |
| `productTaxId` | string | no |  |
| `laborTaxId` | string | no |  |
| `approved` | boolean | no |  |
| `contacts[]` | array<object> | no |  |
| `locations[]` | array<object> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native D-Tools SI API returns.

## Native endpoint

Through the native D-Tools SI API, this operation is `POST https://api.d-tools.com/SI/Publish/Projects` (base URL `https://api.d-tools.com/SI/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-projects.md) for the provider-specific parameters and requirements.


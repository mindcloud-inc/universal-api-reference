# Centerpoint: Create Property



```
POST https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custom.roofSize` | string | no |  |
| `name` | string | yes |  |
| `options.billingAddress` | string | no |  |
| `options.isCreditHold` | boolean | no |  |
| `options.isTaxExempt` | boolean | no |  |
| `accountID` | number | no |  |
| `options.serviceBillingInstructions` | string | no |  |
| `companyID` | list<number> | no |  |
| `options.serviceWorkInstructions` | string | no |  |
| `options.interactivePropertyUrl` | string | no |  |
| `primaryContractorID` | number | no |  |
| `options.taxCodeIDs[]` | array<number> | no |  |
| `primaryBuildingID` | number | no |  |
| `externalID` | string | no |  |
| `importID` | string | no |  |
| `managerID` | number | no |  |
| `locationID` | number | no |  |
| `options` | object | no |  |
| `custom` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Centerpoint API returns.

## Native endpoint

Through the native Centerpoint API, this operation is `POST properties` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-property.md) for the provider-specific parameters and requirements.


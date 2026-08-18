# Centerpoint: Create Company



```
POST https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string",
  "salesStatus": "string",
  "timeZone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string",
    "salesStatus": "string",
    "timeZone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custom.customerType` | string | no |  |
| `name` | string | yes |  |
| `options.taxLabelOverride` | string | no |  |
| `custom.companyPhoneNumber` | string | no |  |
| `options.billingAddress` | string | no |  |
| `type` | list<string> | yes |  |
| `options.isCreditHold` | boolean | no |  |
| `salesStatus` | list<string> | yes |  |
| `options.isTaxExempt` | boolean | no |  |
| `timeZone` | list<string> | yes |  |
| `isBilling` | boolean | no |  |
| `options.serviceBillingInstructions` | string | no |  |
| `isActive` | boolean | no |  |
| `options.serviceWorkInstructions` | string | no |  |
| `email` | string | no |  |
| `options.laborRates` | string | no |  |
| `streetAddress` | string | no |  |
| `subpremise` | string | no |  |
| `locality` | string | no |  |
| `county` | string | no |  |
| `region` | string | no |  |
| `postalCode` | string | no |  |
| `country` | string | no |  |
| `latitude` | number | no |  |
| `longitude` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `placeID` | string | no |  |
| `externalID` | string | no |  |
| `importID` | string | no |  |
| `managerID` | string | no |  |
| `website` | string | no |  |
| `imageID` | string | no |  |
| `closeRate` | number | no | Percentage number between 0 and 1 |
| `options` | object | no |  |
| `custom` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Centerpoint API returns.

## Native endpoint

Through the native Centerpoint API, this operation is `POST companies` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.


# Encircle: Create Property Inspection

Creates a property inspection in Encircle.

```
POST https://connect.mindcloud.co/v1/universal/encircle/latest/actions/create-property-inspection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encircle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/create-property-inspection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "brandId": 1,
  "insurerIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encircle/latest/actions/create-property-inspection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "brandId": 1,
    "insurerIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes |  |
| `brandId` | number | yes |  |
| `insurerIdentifier` | string | yes |  |
| `policyholderName` | string | no |  |
| `fullAddress` | string | no |  |
| `inspectionDate` | date | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `policyholderEmailAddress` | string | no |  |
| `policyholderPhoneNumber` | string | no |  |
| `underwriter` | string | no |  |
| `inspectionCreator` | string | no |  |
| `estimatedBuildingValue` | number | no |  |
| `insuranceCompanyName` | string | no |  |
| `insuranceBrokerName` | string | no |  |
| `policyNumber` | string | no |  |
| `policyRenewalDate` | date | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Encircle API returns.

## Native endpoint

Through the native Encircle API, this operation is `POST /v1/property_inspections` (base URL `https://api.encircleapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-property-inspection.md) for the provider-specific parameters and requirements.


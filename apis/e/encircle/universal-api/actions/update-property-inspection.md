# Encircle: Update Property Inspection

Updates a property inspection in Encircle.

```
PUT https://connect.mindcloud.co/v1/universal/encircle/latest/actions/update-property-inspection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encircle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/update-property-inspection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyInspectionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encircle/latest/actions/update-property-inspection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyInspectionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyInspectionId` | number | yes |  |
| `insurerIdentifier` | string | no |  |
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

Through the native Encircle API, this operation is `PATCH /v1/property_inspections/:property_inspection_id` (base URL `https://api.encircleapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-property-inspection.md) for the provider-specific parameters and requirements.


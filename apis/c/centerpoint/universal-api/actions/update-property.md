# Centerpoint: Update Property



```
PUT https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/update-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/update-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "PROPERTY_ID": "593838"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/update-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "PROPERTY_ID": "593838"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `PROPERTY_ID` | string | yes | Centerpoint property id to update. Use the property id from List Properties. Example: `593838`. |
| `name` | string | no | Centerpoint property name. Example: `CVS - #3425`. |
| `visible` | boolean | no | Whether the Centerpoint property is visible. |
| `timeZone` | string | no | Property timezone, for example America/Chicago. Example: `America/Chicago`. |
| `custom` | object | no | Centerpoint custom fields object. |
| `custom.companyCamProjectId` | string | no | CompanyCam project id linked to this Centerpoint property. Example: `CompanyCam project id`. |
| `custom.companyCamProjectUrl` | string | no | CompanyCam project URL linked to this Centerpoint property. Example: `https://app.companycam.com/projects/...`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountID` | number | no | Centerpoint account id for the property. |
| `companyID` | list<number> | no | Centerpoint company id for the property. |
| `primaryContractorID` | number | no | Centerpoint primary contractor id for the property. |
| `externalID` | string | no | Existing Centerpoint property external id. Do not map CompanyCam here unless this identifier is explicitly owned by the CompanyCam sync. Example: `589466`. |
| `primaryBuildingID` | number | no | Centerpoint primary building id for the property. |
| `importID` | string | no | Centerpoint import id for the property. |
| `managerID` | number | no | Centerpoint manager id for the property. |
| `locationID` | number | no | Centerpoint location id for the property. |
| `options` | object | no | Optional Centerpoint property options object. |
| `options.billingAddress` | string | no | Property billing address in Centerpoint options. |
| `options.isCreditHold` | boolean | no | Whether the property is on credit hold. |
| `options.isTaxExempt` | boolean | no | Whether the property is tax exempt. |
| `options.serviceBillingInstructions` | string | no | Service billing instructions in Centerpoint options. |
| `options.serviceWorkInstructions` | string | no | Service work instructions in Centerpoint options. |
| `options.interactivePropertyUrl` | string | no | Interactive property URL in Centerpoint options. |
| `options.taxCodeIDs[]` | array<number> | no | Centerpoint tax code ids for the property. |
| `custom.roofSize` | string | no | Property roof size custom field. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Centerpoint API returns.

## Native endpoint

Through the native Centerpoint API, this operation is `PATCH properties/:PROPERTY_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-property.md) for the provider-specific parameters and requirements.


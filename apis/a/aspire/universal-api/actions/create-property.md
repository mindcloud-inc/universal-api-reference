# Aspire: Create Property



```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "PropertyName": "Ava Chen",
  "BranchID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "PropertyName": "Ava Chen",
    "BranchID": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `PropertyName` | string | yes |  |
| `PropertyNameAbr` | string | no |  |
| `PrimaryContactID` | list<number> | no | Choose an option from the list or map the Contact ID from a previous step. |
| `BranchID` | list<number> | yes |  |
| `TaxJurisdictionId` | list<number> | no |  |
| `PaymentTermsID` | list<number> | no |  |
| `PropertyStatusID` | list<number> | no |  |
| `AccountOwnerContactID` | list<number> | no |  |
| `AddressLine1` | string | no |  |
| `AddressLine2` | string | no |  |
| `City` | string | no |  |
| `StateProvinceCode` | string | no | Enter a US state, US territory, or Canadian province. Use the two-letter UPS code (e.g., "IL" for Illinois, "ON" for Ontario) or enter the full name and we'll convert it to the two-letter code based on the input. Reference this list for available options: https://www.ups.com/worldshiphelp/WSA/ENU/AppHelp/mergedProjects/CORE/Codes/State_Province_Codes.htm |
| `ZipCode` | string | no |  |
| `Active` | boolean | no |  |
| `PaperlessInvoices` | boolean | no |  |
| `EmailInvoiceFlag` | boolean | no |  |
| `LeadSourceID` | number | no |  |
| `IndustryID` | number | no |  |
| `BillingContactID` | list<number> | no |  |
| `PropertyTags` | string | no |  |
| `ProductionManagerContactID` | list | no |  |
| `CountyID` | number | no | Use this when Locality is enabled |
| `Note` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "propertyID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `propertyID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `POST Properties` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-property.md) for the provider-specific parameters and requirements.


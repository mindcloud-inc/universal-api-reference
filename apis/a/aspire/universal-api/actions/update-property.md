# Aspire: Update Property

Updates a Property in Aspire

```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "PropertyID": 1,
  "PropertyName": "Ava Chen",
  "BranchID": 1,
  "PaymentTermsID": 1,
  "PropertyStatusID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "PropertyID": 1,
    "PropertyName": "Ava Chen",
    "BranchID": 1,
    "PaymentTermsID": 1,
    "PropertyStatusID": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `PropertyID` | list<number> | yes |  |
| `PropertyName` | string | yes |  |
| `PrimaryContactID` | list<number> | no |  |
| `Billing Contact ID` | list<number> | no |  |
| `BranchID` | list<number> | yes |  |
| `AccountOwnerContactID` | list<number> | no |  |
| `TaxJurisdictionID` | list<number> | no |  |
| `PaymentTermsID` | list<number> | yes |  |
| `PropertyStatusID` | list<number> | yes |  |
| `StateProvinceCode` | string | no |  |
| `AddressLine1` | string | no |  |
| `Address Line 2` | string | no |  |
| `City` | string | no |  |
| `ZipCode` | string | no |  |
| `active` | boolean | no |  |
| `ProductionNote` | string | no |  |
| `Note` | string | no |  |
| `PropertyNameAbr` | string | no |  |
| `CountyID` | number | no |  |
| `GEOPerimeter` | number | no |  |
| `SequenceNumber` | string | no |  |
| `Budget` | number | no |  |
| `SeparateInvoices` | boolean | no |  |
| `EmailInvoiceFlag` | boolean | no |  |
| `UpdateBranchReference` | boolean | no |  |
| `IndustryID` | number | no |  |
| `LeadSourceID` | number | no |  |
| `CompetitorID` | number | no |  |
| `PropertyGroupID` | list<number> | no |  |
| `Note` | string | no |  |
| `SnowNote` | string | no |  |
| `CollectionNotes` | string | no |  |
| `IntegrationID` | number | no |  |
| `PropertyTypeID` | list<number> | no |  |
| `productionManagerContactID` | list<number> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `PUT Properties` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-property.md) for the provider-specific parameters and requirements.


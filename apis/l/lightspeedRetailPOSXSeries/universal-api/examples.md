# Lightspeed Retail POS (X-Series) Universal API Examples

These examples use the MindCloud API key and Lightspeed Retail POS (X-Series) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Retailer

Retrieves retailer information from Lightspeed Retail POS (X-Series).

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-retailer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-retailer?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "accountStatus": "string",
      "accountType": "string",
      "activatedAt": "2026-05-07T12:00:00.000Z",
      "country": "string",
      "createCustomerByEmailReceipt": "ava@example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "culture": "string",
      "currency": {},
      "defaultDimensionsUnit": "string",
      "defaultTaxId": "string",
      "defaultWeightUnit": "string",
      "disableOnboardingTour": true,
      "discountProductId": "string",
      "domainPrefix": "string",
      "ecwidOnboardingSurveyState": "string",
      "embeddedBarcodeOption": "string",
      "enabledIntegrations": [
        {}
      ],
      "enabledPlatformApps": [
        {}
      ],
      "enableLineItemConsolidation": true,
      "giftCards": {},
      "hasWebRegister": true,
      "id": "string",
      "labelPrinterFormat": "string",
      "lightspeedUniqueId": "string",
      "loyalty": {},
      "marketCode": "string",
      "marketSegment": "string",
      "name": "Ava Chen",
      "noTaxGroupId": "string",
      "onAccount": {},
      "registerMigrationDate": "2026-05-07T12:00:00.000Z",
      "requirePasswordOnUserSwitch": "string",
      "restrictionState": "string",
      "restrictionStateReason": "string",
      "signupIndustryVertical": "string",
      "skuSequence": {},
      "ssoEnabled": true,
      "storeCredit": true,
      "storeUrl": "https://example.com",
      "subscription": {},
      "subscriptionPlanVersion": 1,
      "taxExclusive": true,
      "termsAndConditions": {},
      "timezone": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Retailer action reference](actions/get-retailer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lightspeedRetailPOSXSeries/latest/actions/get-retailer).

## Create Customer

Creates a new customer in Lightspeed Retail POS (X-Series).

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "balance": "string",
      "companyName": "Ava Chen",
      "contactSource": "string",
      "createdAt": "string",
      "customerCode": "string",
      "customerGroupId": "string",
      "customerGroupIds": "string",
      "customField1": "string",
      "customField2": "string",
      "customField3": "string",
      "customField4": "string",
      "dateOfBirth": "string",
      "deletedAt": "string",
      "doNotEmail": "ava@example.com",
      "email": "ava@example.com",
      "enableLoyalty": "string",
      "enablePromotionalSms": "string",
      "fax": "string",
      "firstName": "Ava",
      "gender": "string",
      "id": "string",
      "lastName": "Chen",
      "loyaltyBalance": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "note": "string",
      "onAccountLimit": "string",
      "phone": "string",
      "physicalAddress1": "string",
      "physicalAddress2": "string",
      "physicalCity": "string",
      "physicalCountryId": "string",
      "physicalPostcode": "string",
      "physicalState": "string",
      "physicalSuburb": "string",
      "postalAddress1": "string",
      "postalAddress2": "string",
      "postalCity": "string",
      "postalCountryId": "string",
      "postalPostcode": "string",
      "postalState": "string",
      "postalSuburb": "string",
      "taxId": "string",
      "twitter": "string",
      "updatedAt": "string",
      "version": "string",
      "website": "string",
      "yearToDate": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lightspeedRetailPOSXSeries/latest/actions/create-customer).

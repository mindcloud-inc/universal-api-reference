# Viewpoint Spectrum: Update Vendor (SOAP)



```
PUT https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/update-vendor-soap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/update-vendor-soap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vendorCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/update-vendor-soap', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vendorCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vendorCode` | string | yes | Vendor Code. |
| `vendorName` | string | no | Vendor Name. |
| `alphaSort` | string | no | Vendor Alpha Ref. |
| `type` | string | no | Vendor Type. |
| `ourAccountNumber` | string | no | Account reference. |
| `address1` | string | no | Address 1. |
| `address2` | string | no | Address 2. |
| `city` | string | no | City. |
| `state` | string | no | State/province. |
| `zipCode` | string | no | Postal code. |
| `addrCountry` | string | no | Country. |
| `phone` | string | no | Phone Number. |
| `faxPhone` | string | no | Fax number. |
| `vendorEmail` | string | no | Vendor email. |
| `webSite` | string | no | Website. |
| `status` | string | no | Status: A, I, or N. |
| `routingCode1` | string | no | Routing Code for Invoice Approval. |
| `routingLimit` | number | no | Routing limit invoice approval. |
| `routingCode2` | string | no | Routing Code for Over Limit Invoice Approval. |
| `useTaxCode` | string | no | Sales/Use Tax Code. |
| `defaultGLAccount` | string | no | Default G/L Code. |
| `holdFlag` | string | no | On hold flag (Y/N). |
| `termsCode` | string | no | Payment due terms (A or B only). |
| `termsDays` | number | no | Days Payment Due. |
| `termsDiscCode` | string | no | Discount Due (A or B only). |
| `termsDiscDays` | number | no | Days Discount Due. |
| `termsDiscPercent` | number | no | Discount percent. |
| `insuranceCertFlag` | string | no | Insurance certificate flag (Y/N). |
| `insuranceExpDate` | date | no | Insurance expiration date. |
| `pOMethod` | string | no | Purchase order default method. |
| `vendorStatus` | string | no | Payment method. |
| `checkingAccountCode` | string | no | Electronic payment account code. |
| `accountType` | string | no | Electronic payment account type. |
| `aBANumber` | string | no | Electronic payment ABA routing number. |
| `send1099Flag` | string | no | 1099 flag (Y/N). |
| `alt1099Name` | string | no | Alternate 1099 name. |
| `fed1099Indicator` | string | no | 1099 payment indicator. |
| `socialSecNumber` | string | no | Social Security number. |
| `fedIdNumber` | string | no | Federal ID number. |
| `overrideCurrencyCode` | string | no | Override Currency Code. |
| `recipientTypeCode` | string | no | Canadian T5018 recipient type code. |
| `socialInsuranceNumber` | string | no | Canadian T5018 social insurance number. |
| `recipientAccountNumber` | string | no | Canadian T5018 recipient account number. |
| `partnershipFilerIDNumber` | string | no | Canadian T5018 partnership filer ID number. |
| `alternateT5018Name` | string | no | Canadian T5018 alternate name. |
| `individualFirstName` | string | no | Canadian T5018 individual first name. |
| `individualMiddleInitial` | string | no | Canadian T5018 individual middle initial. |
| `individualLastName` | string | no | Canadian T5018 individual last name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/UpdateVendor` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor-soap.md) for the provider-specific parameters and requirements.


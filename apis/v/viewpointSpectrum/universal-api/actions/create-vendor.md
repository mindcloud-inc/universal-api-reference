# Viewpoint Spectrum: Create Vendor



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vendorCode": "string",
  "vendorName": "Ava Chen",
  "alphaSort": "string",
  "termsCode": "string",
  "termsDays": 1,
  "termsDiscCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vendorCode": "string",
    "vendorName": "Ava Chen",
    "alphaSort": "string",
    "termsCode": "string",
    "termsDays": 1,
    "termsDiscCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vendorCode` | string | yes | Vendor Code. |
| `vendorName` | string | yes | Vendor Name. |
| `alphaSort` | string | yes | Vendor Alpha Ref. |
| `type` | string | no | Vendor Type. |
| `address1` | string | no | Address 1. |
| `address2` | string | no | Address 2. |
| `city` | string | no | City. |
| `state` | string | no | State/province. |
| `zipCode` | string | no | Postal code. |
| `phone` | string | no | Phone Number. |
| `faxPhone` | string | no | Fax number. |
| `contactName` | string | no | Contact Name. |
| `ourAccountNumber` | string | no | Account reference. |
| `termsCode` | string | yes | Payment due terms (A or B only). |
| `termsDays` | number | yes | Days Payment Due. |
| `termsDiscCode` | string | yes | Discount Due (A or B only). |
| `termsDiscDays` | number | no | Days Discount Due. |
| `termsDiscPercent` | number | no | Discount percent. |
| `insuranceCertFlag` | string | no | Insurance certificate flag (Y/N). |
| `insuranceExpDate` | date | no | Insurance expiration date. |
| `holdFlag` | string | no | On hold flag (Y/N). |
| `defaultGLAccount` | string | no | Default G/L Code. |
| `useTaxCode` | string | no | Sales/Use Tax Code. |
| `send1099Flag` | string | no | 1099 flag (Y/N). |
| `alt1099Name` | string | no | Alternate 1099 name. |
| `fed1099Indicator` | string | no | 1099 payment indicator. |
| `socialSecNumber` | string | no | Social Security number. |
| `fedIdNumber` | string | no | Federal ID number. |
| `vendorEmail` | string | no | Vendor email. |
| `contactPhone` | string | no | Contact phone. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/AddVendor` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor.md) for the provider-specific parameters and requirements.


# Zahara: List Suppliers After Date

Retrieves suppliers from Zahara after a specific date.

```
GET https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-suppliers-after-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-suppliers-after-date?connectionId=$CONNECTION_ID&date=2020-12-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2020-12-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-suppliers-after-date?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | yes | Return suppliers updated after this date. Example: `2020-12-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address": {
        "AddressId": 1,
        "AddressLines": "string",
        "AddressType": 1,
        "CountryCode": "string",
        "CountryCodeId": 1,
        "IsPrimary": true,
        "LastUpdated": "2026-05-07T12:00:00.000Z",
        "Postcode": "string",
        "Void": true
      },
      "BankAccountNumber": "string",
      "BankSortCode": "string",
      "BusinessUnitId": 1,
      "ContactName": "Ava Chen",
      "CountryCode": "string",
      "CountryCodeId": 1,
      "DateCreated": "2026-05-07T12:00:00.000Z",
      "DefaultCostCode": "string",
      "DefaultCostCodeId": 1,
      "DefaultCurrencyId": 1,
      "DefaultNominalCode": "string",
      "DefaultNominalCodeId": 1,
      "DefaultPaymentTerms": 1,
      "DefaultTaxCode": "string",
      "DefaultTaxCodeId": 1,
      "Email": "ava@example.com",
      "IsActive": true,
      "LastUpdated": "2026-05-07T12:00:00.000Z",
      "PaymentTermDaysNumber": 1,
      "PaymentTermStartType": 1,
      "PaymentTermType": 1,
      "ReferenceNumber": "string",
      "SupplierEmails": [
        {
          "AddedOn": "2026-05-07T12:00:00.000Z",
          "Email": "ava@example.com",
          "SupplierEmailId": 1,
          "SupplierEmailType": 1,
          "SupplierEmailTypeDescription": "ava@example.com"
        }
      ],
      "SupplierId": 1,
      "SupplierName": "Ava Chen",
      "TrustedStatus": true,
      "Void": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address.AddressId` | number | Supplier address ID. |
| `Address.AddressLines` | string | Supplier address lines. |
| `Address.AddressType` | number | Supplier address type. |
| `Address.CountryCode` | string | Supplier country code. |
| `Address.CountryCodeId` | number | Supplier country code ID. |
| `Address.IsPrimary` | boolean | Whether the supplier address is primary. |
| `Address.LastUpdated` | date | Supplier address last update timestamp. |
| `Address.Postcode` | string | Supplier postcode. |
| `Address.Void` | boolean | Whether the supplier address is void. |
| `BankAccountNumber` | string | Supplier bank account number. |
| `BankSortCode` | string | Supplier bank sort code. |
| `BusinessUnitId` | number | Business unit ID. |
| `ContactName` | string | Supplier contact name. |
| `CountryCode` | string | Supplier country code. |
| `CountryCodeId` | number | Supplier country code ID. |
| `DateCreated` | date | Creation timestamp. |
| `DefaultCostCode` | string | Default cost code. |
| `DefaultCostCodeId` | number | Default cost code ID. |
| `DefaultCurrencyId` | number | Default currency ID. |
| `DefaultNominalCode` | string | Default nominal code. |
| `DefaultNominalCodeId` | number | Default nominal code ID. |
| `DefaultPaymentTerms` | number | Default payment terms. |
| `DefaultTaxCode` | string | Default tax code. |
| `DefaultTaxCodeId` | number | Default tax code ID. |
| `Email` | string | Supplier email address. |
| `IsActive` | boolean | Whether the supplier is active. |
| `LastUpdated` | date | Last update timestamp. |
| `PaymentTermDaysNumber` | number | Payment term day count. |
| `PaymentTermStartType` | number | Payment term start type. |
| `PaymentTermType` | number | Payment term type. |
| `ReferenceNumber` | string | Supplier reference number. |
| `SupplierEmails[].AddedOn` | date | Supplier email added timestamp. |
| `SupplierEmails[].Email` | string | Supplier email entry. |
| `SupplierEmails[].SupplierEmailId` | number | Supplier email ID. |
| `SupplierEmails[].SupplierEmailType` | number | Supplier email type. |
| `SupplierEmails[].SupplierEmailTypeDescription` | string | Supplier email type description. |
| `SupplierId` | number | Supplier ID. |
| `SupplierName` | string | Supplier name. |
| `TrustedStatus` | boolean | Trusted supplier flag. |
| `Void` | boolean | Whether the supplier is void. |

## Native endpoint

Through the native Zahara API, this operation is `GET /api/{{credentials.businessUnitApiKey}}/Supplier/After/{{date}}` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suppliers-after-date.md) for the provider-specific parameters and requirements.


# IRIS KashFlow: Get Company Details



```
GET https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-company-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IRIS KashFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-company-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-company-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Address1": "string",
      "Address2": "string",
      "Address3": "string",
      "Address4": "string",
      "BusinessType": "string",
      "BusinessType1": "string",
      "BusinessType1Name": "Ava Chen",
      "BusinessType2": "string",
      "BusinessType2Name": "Ava Chen",
      "BusinessType3": "string",
      "BusinessType3Name": "Ava Chen",
      "CompanyName": "Ava Chen",
      "CurrencyId": "string",
      "CurrencyName": "Ava Chen",
      "CurrencyPosition": "string",
      "CurrencySymbol": "string",
      "Mobile": "string",
      "PaymentTerms": "string",
      "PaymentTermsType": "string",
      "Postcode": "string",
      "PrimaryContact": "string",
      "PrimaryEmail": "ava@example.com",
      "Telephone": "string",
      "UsDate": "string",
      "VatRegistered": "string",
      "VatRegistrationNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address1` | string |  |
| `Address2` | string |  |
| `Address3` | string |  |
| `Address4` | string |  |
| `BusinessType` | string |  |
| `BusinessType1` | string |  |
| `BusinessType1Name` | string |  |
| `BusinessType2` | string |  |
| `BusinessType2Name` | string |  |
| `BusinessType3` | string |  |
| `BusinessType3Name` | string |  |
| `CompanyName` | string |  |
| `CurrencyId` | string |  |
| `CurrencyName` | string |  |
| `CurrencyPosition` | string |  |
| `CurrencySymbol` | string |  |
| `Mobile` | string |  |
| `PaymentTerms` | string |  |
| `PaymentTermsType` | string |  |
| `Postcode` | string |  |
| `PrimaryContact` | string |  |
| `PrimaryEmail` | string |  |
| `Telephone` | string |  |
| `UsDate` | string |  |
| `VatRegistered` | string |  |
| `VatRegistrationNumber` | string |  |

## Native endpoint

Through the native IRIS KashFlow API, this operation is `POST /api/service.asmx` (base URL `https://securedwebapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-details.md) for the provider-specific parameters and requirements.


# SAP ERP (S/4HANA): Get Related Business Partner

Retrieves a related business partner from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-related-business-partner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-related-business-partner?connectionId=$CONNECTION_ID&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-related-business-partner?${params}`, {
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
| `businessPartner` | string | yes | Business partner identifier such as 11. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bpBalanceSheetCurrency": "string",
      "bpLastCapitalIncreaseYear": "string",
      "bpLastCptlIncrAmtInBalShtCrcy": "string",
      "bpRegisteredOfficeName": "Ava Chen",
      "businessPartner": "string",
      "businessPartnerIsEmployee": true,
      "businessPartnerIsVIP": true,
      "businessPartnerOfficeCountry": "string",
      "businessPartnerOfficeRegion": "string",
      "customerIsUnwanted": true,
      "factoryCalendar": "string",
      "lastCustomerContactDate": "2026-05-07T12:00:00.000Z",
      "tradingPartner": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bpBalanceSheetCurrency` | string | Balance sheet currency. |
| `bpLastCapitalIncreaseYear` | string | Last capital increase year. |
| `bpLastCptlIncrAmtInBalShtCrcy` | string | Last capital increase amount in balance sheet currency. |
| `bpRegisteredOfficeName` | string | Registered office name. |
| `businessPartner` | string | Business partner identifier. |
| `businessPartnerIsEmployee` | boolean | Whether the business partner is an employee. |
| `businessPartnerIsVIP` | boolean | Whether the business partner is marked as VIP. |
| `businessPartnerOfficeCountry` | string | Office country code. |
| `businessPartnerOfficeRegion` | string | Office region code. |
| `customerIsUnwanted` | boolean | Whether the customer is marked as unwanted. |
| `factoryCalendar` | string | Factory calendar code. |
| `lastCustomerContactDate` | date | Date of the last customer contact. |
| `tradingPartner` | string | Trading partner code. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartner` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-related-business-partner.md) for the provider-specific parameters and requirements.


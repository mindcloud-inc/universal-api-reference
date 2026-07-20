# SAP ERP (S/4HANA): Get Business Partner Credit Worthiness

Retrieves credit worthiness for a business partner from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-business-partner-credit-worthiness
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-business-partner-credit-worthiness?connectionId=$CONNECTION_ID&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-business-partner-credit-worthiness?${params}`, {
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
      "BPCrdtWrthnssAccessChkIsActive": "string",
      "BPCreditStandingComment": "string",
      "BPCreditStandingDate": "2026-05-07T12:00:00.000Z",
      "BPCreditStandingRating": "string",
      "BPCreditStandingStatus": "string",
      "BPForeclosureDate": "2026-05-07T12:00:00.000Z",
      "BPForeclosureIsInitiated": true,
      "BPLegalProceedingStatus": "string",
      "BPLglProceedingInitiationDate": "2026-05-07T12:00:00.000Z",
      "BusinessPartner": "string",
      "BusinessPartnerBankruptcyDate": "2026-05-07T12:00:00.000Z",
      "BusinessPartnerIsBankrupt": true,
      "BusinessPartnerIsUnderOath": true,
      "BusinessPartnerOathDate": "2026-05-07T12:00:00.000Z",
      "BusPartCreditStanding": "string",
      "CreditRatingAgency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BPCrdtWrthnssAccessChkIsActive` | string |  |
| `BPCreditStandingComment` | string |  |
| `BPCreditStandingDate` | date |  |
| `BPCreditStandingRating` | string |  |
| `BPCreditStandingStatus` | string |  |
| `BPForeclosureDate` | date |  |
| `BPForeclosureIsInitiated` | boolean |  |
| `BPLegalProceedingStatus` | string |  |
| `BPLglProceedingInitiationDate` | date |  |
| `BusinessPartner` | string |  |
| `BusinessPartnerBankruptcyDate` | date |  |
| `BusinessPartnerIsBankrupt` | boolean |  |
| `BusinessPartnerIsUnderOath` | boolean |  |
| `BusinessPartnerOathDate` | date |  |
| `BusPartCreditStanding` | string |  |
| `CreditRatingAgency` | string |  |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner('{{businessPartner}}')/to_BPCreditWorthiness` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business-partner-credit-worthiness.md) for the provider-specific parameters and requirements.


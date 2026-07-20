# SAP ERP (S/4HANA): List Business Partner Addresses

Retrieves addresses for a business partner from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-addresses?connectionId=$CONNECTION_ID&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-addresses?${params}`, {
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
      "addressId": "string",
      "addressUUID": "string",
      "businessPartner": "string",
      "cityName": "Ava Chen",
      "country": "string",
      "fullName": "Ava Chen",
      "houseNumber": "string",
      "postalCode": "string",
      "streetName": "Ava Chen",
      "validityEndDate": "2026-05-07T12:00:00.000Z",
      "validityStartDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressId` | string | Address identifier. |
| `addressUUID` | string | Address UUID. |
| `businessPartner` | string | Business partner identifier. |
| `cityName` | string | City name. |
| `country` | string | Country code. |
| `fullName` | string | Full address name. |
| `houseNumber` | string | House number. |
| `postalCode` | string | Postal code. |
| `streetName` | string | Street name. |
| `validityEndDate` | date | Validity end date. |
| `validityStartDate` | date | Validity start date. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartnerAddress` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-partner-addresses.md) for the provider-specific parameters and requirements.


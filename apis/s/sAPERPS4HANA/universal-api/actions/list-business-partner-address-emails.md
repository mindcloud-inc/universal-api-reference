# SAP ERP (S/4HANA): List Business Partner Address Emails

Retrieves business partner address emails from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-address-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-address-emails?connectionId=$CONNECTION_ID&addressId=string&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "addressId": "string",
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-address-emails?${params}`, {
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
| `addressId` | string | yes | Address identifier such as 27512. |
| `businessPartner` | string | yes | Business partner identifier such as 11. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AddressCommunicationRemarkText": "string",
      "AddressID": "string",
      "EmailAddress": "ava@example.com",
      "IsDefaultEmailAddress": true,
      "OrdinalNumber": "string",
      "Person": "string",
      "SearchEmailAddress": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AddressCommunicationRemarkText` | string |  |
| `AddressID` | string |  |
| `EmailAddress` | string |  |
| `IsDefaultEmailAddress` | boolean |  |
| `OrdinalNumber` | string |  |
| `Person` | string |  |
| `SearchEmailAddress` | string |  |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartnerAddress(BusinessPartner='{{businessPartner}}',AddressID='{{addressId}}')/to_EmailAddress` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-partner-address-emails.md) for the provider-specific parameters and requirements.


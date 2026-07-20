# SAP ERP (S/4HANA): List Address Independent Emails

Retrieves address-independent emails from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-address-independent-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-address-independent-emails?connectionId=$CONNECTION_ID&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-address-independent-emails?${params}`, {
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
      "AddressID": "string",
      "BusinessPartner": "string",
      "EmailAddress": "ava@example.com",
      "IsDefaultEmailAddress": true,
      "OrdinalNumber": "string",
      "Person": "string",
      "ValidityEndDate": "2026-05-07T12:00:00.000Z",
      "ValidityStartDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AddressID` | string |  |
| `BusinessPartner` | string |  |
| `EmailAddress` | string |  |
| `IsDefaultEmailAddress` | boolean |  |
| `OrdinalNumber` | string |  |
| `Person` | string |  |
| `ValidityEndDate` | date |  |
| `ValidityStartDate` | date |  |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner('{{businessPartner}}')/to_AddressIndependentEmail` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-address-independent-emails.md) for the provider-specific parameters and requirements.


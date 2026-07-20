# SAP ERP (S/4HANA): List Business Partner Data Controllers

Retrieves data controllers for a business partner from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-data-controllers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-data-controllers?connectionId=$CONNECTION_ID&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-data-controllers?${params}`, {
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
      "BPDataControllerIsDerived": "string",
      "BusinessPartner": "string",
      "BusinessPurposeFlag": "string",
      "DataControlAssignmentStatus": "string",
      "DataController": "string",
      "PurposeDerived": "string",
      "PurposeForPersonalData": "string",
      "PurposeType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BPDataControllerIsDerived` | string |  |
| `BusinessPartner` | string |  |
| `BusinessPurposeFlag` | string |  |
| `DataControlAssignmentStatus` | string |  |
| `DataController` | string |  |
| `PurposeDerived` | string |  |
| `PurposeForPersonalData` | string |  |
| `PurposeType` | string |  |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner('{{businessPartner}}')/to_BPDataController` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-partner-data-controllers.md) for the provider-specific parameters and requirements.


# SAP ERP (S/4HANA): List Business Partner Relationships

Retrieves relationships for a business partner from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-relationships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-relationships?connectionId=$CONNECTION_ID&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-relationships?${params}`, {
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
      "BPRelationshipType": "string",
      "BusinessPartner1": "string",
      "BusinessPartner2": "string",
      "CreatedByUser": "string",
      "CreationDate": "2026-05-07T12:00:00.000Z",
      "CreationTime": "2026-05-07T12:00:00.000Z",
      "IsStandardRelationship": true,
      "LastChangeDate": "2026-05-07T12:00:00.000Z",
      "LastChangedByUser": "string",
      "LastChangeTime": "2026-05-07T12:00:00.000Z",
      "RelationshipCategory": "string",
      "RelationshipNumber": "string",
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
| `BPRelationshipType` | string |  |
| `BusinessPartner1` | string |  |
| `BusinessPartner2` | string |  |
| `CreatedByUser` | string |  |
| `CreationDate` | date |  |
| `CreationTime` | date |  |
| `IsStandardRelationship` | boolean |  |
| `LastChangeDate` | date |  |
| `LastChangedByUser` | string |  |
| `LastChangeTime` | date |  |
| `RelationshipCategory` | string |  |
| `RelationshipNumber` | string |  |
| `ValidityEndDate` | date |  |
| `ValidityStartDate` | date |  |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner('{{businessPartner}}')/to_BPRelationship` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-partner-relationships.md) for the provider-specific parameters and requirements.


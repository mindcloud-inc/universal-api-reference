# Aspire: List Equipment Requested Services

Retrieves equipment requested services from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipment-requested-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipment-requested-services?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipment-requested-services?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedByUserID": 1,
      "CreatedByUserName": "Ava Chen",
      "CreatedDateTime": "2026-05-07T12:00:00.000Z",
      "EquipmentID": 1,
      "EquipmentInspectionCategoryID": 1,
      "EquipmentInspectionCategoryName": "Ava Chen",
      "EquipmentInspectionID": 1,
      "EquipmentRequestedServiceID": 1,
      "EquipmentServiceLogID": 1,
      "EquipmentServiceTagID": 1,
      "LastModifiedByUserID": 1,
      "LastModifiedByUserName": "Ava Chen",
      "LastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "Notes": "string",
      "RequestSource": "string",
      "ServiceTagName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedByUserID` | number |  |
| `CreatedByUserName` | string |  |
| `CreatedDateTime` | date |  |
| `EquipmentID` | number |  |
| `EquipmentInspectionCategoryID` | number |  |
| `EquipmentInspectionCategoryName` | string |  |
| `EquipmentInspectionID` | number |  |
| `EquipmentRequestedServiceID` | number |  |
| `EquipmentServiceLogID` | number |  |
| `EquipmentServiceTagID` | number |  |
| `LastModifiedByUserID` | number |  |
| `LastModifiedByUserName` | string |  |
| `LastModifiedDateTime` | date |  |
| `Notes` | string |  |
| `RequestSource` | string |  |
| `ServiceTagName` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET EquipmentRequestedServices` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-equipment-requested-services.md) for the provider-specific parameters and requirements.


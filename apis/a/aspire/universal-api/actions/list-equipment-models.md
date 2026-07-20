# Aspire: List Equipment Models

Retrieves equipment models from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipment-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipment-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipment-models?${params}`, {
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
      "Active": true,
      "CapEXMonths": 1,
      "CreatedByUserID": 1,
      "CreatedByUserName": "Ava Chen",
      "CreatedDateTime": "2026-05-07T12:00:00.000Z",
      "EquipmentClassID": 1,
      "EquipmentClassName": "Ava Chen",
      "EquipmentManufacturerID": 1,
      "EquipmentManufacturerName": "Ava Chen",
      "EquipmentModelID": 1,
      "EquipmentSizeID": 1,
      "EquipmentSizeName": "Ava Chen",
      "FuelBurnRate": 1,
      "FuelUnit": "string",
      "LastModifiedByUserID": 1,
      "LastModifiedByUserName": "Ava Chen",
      "LastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "MeterType": "string",
      "ModelName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `CapEXMonths` | number |  |
| `CreatedByUserID` | number |  |
| `CreatedByUserName` | string |  |
| `CreatedDateTime` | date |  |
| `EquipmentClassID` | number |  |
| `EquipmentClassName` | string |  |
| `EquipmentManufacturerID` | number |  |
| `EquipmentManufacturerName` | string |  |
| `EquipmentModelID` | number |  |
| `EquipmentSizeID` | number |  |
| `EquipmentSizeName` | string |  |
| `FuelBurnRate` | number |  |
| `FuelUnit` | string |  |
| `LastModifiedByUserID` | number |  |
| `LastModifiedByUserName` | string |  |
| `LastModifiedDateTime` | date |  |
| `MeterType` | string |  |
| `ModelName` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET EquipmentModels` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-equipment-models.md) for the provider-specific parameters and requirements.


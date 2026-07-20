# InventoryBase: Get Inspection Report Metadata

Retrieves inspection report metadata from InventoryBase.

```
GET https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-inspection-report-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-inspection-report-metadata?connectionId=$CONNECTION_ID&inspectionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inspectionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-inspection-report-metadata?${params}`, {
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
| `inspectionId` | number | yes | The ID of the inspection |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alarms": [
        {}
      ],
      "keys": [
        {}
      ],
      "manuals": [
        {}
      ],
      "meters": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alarms` | array<object> |  |
| `keys` | array<object> |  |
| `manuals` | array<object> |  |
| `meters` | array<object> |  |

## Native endpoint

Through the native InventoryBase API, this operation is `GET /inspections/:inspectionId/report/metadata` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inspection-report-metadata.md) for the provider-specific parameters and requirements.


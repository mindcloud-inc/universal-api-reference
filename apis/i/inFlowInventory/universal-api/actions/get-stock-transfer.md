# inFlow Inventory: Get Stock Transfer

Retrieves an existing stock transfer from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-stock-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-stock-transfer?connectionId=$CONNECTION_ID&stockTransferId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stockTransferId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-stock-transfer?${params}`, {
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
| `stockTransferId` | string | yes | The unique identifier of the stock transfer to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToTeamMemberId": "string",
      "fromLocationId": "string",
      "isCancelled": true,
      "lastModifiedById": "string",
      "receivedDate": "2026-05-07T12:00:00.000Z",
      "remarks": "string",
      "sentDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "stockTransferId": "string",
      "timestamp": "string",
      "toLocationId": "string",
      "transferDate": "2026-05-07T12:00:00.000Z",
      "transferNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToTeamMemberId` | string |  |
| `fromLocationId` | string |  |
| `isCancelled` | boolean |  |
| `lastModifiedById` | string |  |
| `receivedDate` | date |  |
| `remarks` | string |  |
| `sentDate` | date |  |
| `status` | string |  |
| `stockTransferId` | string |  |
| `timestamp` | string |  |
| `toLocationId` | string |  |
| `transferDate` | date |  |
| `transferNumber` | string |  |

## Native endpoint

Through the native inFlow Inventory API, this operation is `GET /stock-transfers/:stockTransferId` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock-transfer.md) for the provider-specific parameters and requirements.


# Seven Time: List Time Logs

Retrieves time logs from a Seven Time workspace.

```
GET https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-time-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven Time `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-time-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-time-logs?${params}`, {
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
| `user` | string | no | Filter time logs by user id. |
| `customer` | string | no | Filter time logs by customer id. |
| `project` | string | no | Filter time logs by project id. |
| `task` | string | no | Filter time logs by task id. |
| `category` | string | no | Filter time logs by category id. |
| `workOrder` | string | no | Filter time logs by work order id. |
| `workOrderNumber` | string | no | Filter time logs by work order number. |
| `timestamp` | date | no | Include time logs that start after the given timestamp. |
| `endTimestamp` | date | no | Include time logs that end before the given timestamp. |
| `invoicedDate` | date | no | Include time logs invoiced since the given timestamp. |
| `isAbsence` | boolean | no | Filter time logs by absence status. |
| `lastModified` | date | no | Include time logs modified since the given timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allDay": true,
      "cost": 1,
      "createDate": "2026-05-07T12:00:00.000Z",
      "customer": "string",
      "customFields": [
        {}
      ],
      "description": "string",
      "endTimestamp": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "invoiceableTime": 1,
      "isInvoiceable": true,
      "isInvoiced": true,
      "isWorkTime": true,
      "machineTimePrices": [
        {}
      ],
      "machineTimeSupplements": [
        {}
      ],
      "project": "string",
      "realTimestamp": "2026-05-07T12:00:00.000Z",
      "startLocation": {},
      "status": 1,
      "stopLocation": {},
      "time": 1,
      "timeCategory": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "unSocialHoursCosts": [
        {}
      ],
      "user": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allDay` | boolean |  |
| `cost` | number |  |
| `createDate` | date |  |
| `customer` | string |  |
| `customFields` | array<object> |  |
| `description` | string |  |
| `endTimestamp` | date |  |
| `Id` | string |  |
| `invoiceableTime` | number |  |
| `isInvoiceable` | boolean |  |
| `isInvoiced` | boolean |  |
| `isWorkTime` | boolean |  |
| `machineTimePrices` | array<object> |  |
| `machineTimeSupplements` | array<object> |  |
| `project` | string |  |
| `realTimestamp` | date |  |
| `startLocation` | object |  |
| `status` | number |  |
| `stopLocation` | object |  |
| `time` | number |  |
| `timeCategory` | string |  |
| `timestamp` | date |  |
| `unSocialHoursCosts` | array<object> |  |
| `user` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Seven Time API, this operation is `GET /timeLogs` (base URL `https://app.seventime.se/api/2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-logs.md) for the provider-specific parameters and requirements.


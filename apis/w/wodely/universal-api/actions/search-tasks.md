# Wodely: Search Tasks



```
GET https://connect.mindcloud.co/v1/universal/wodely/latest/actions/search-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/search-tasks?connectionId=$CONNECTION_ID&startDateTime=2026-03-27T00%3A00%3A00Z&endDateTime=2026-03-27T23%3A59%3A59Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDateTime": "2026-03-27T00:00:00Z",
  "endDateTime": "2026-03-27T23:59:59Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wodely/latest/actions/search-tasks?${params}`, {
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
| `startDateTime` | string | yes | UTC ISO 8601 start of the search window. Example: `2026-03-27T00:00:00Z`. |
| `endDateTime` | string | yes | UTC ISO 8601 end of the search window. Example: `2026-03-27T23:59:59Z`. |
| `taskStatusId` | string | no | Filter tasks by Wodely task status identifier. |
| `taskTypeId` | string | no | Filter tasks by Wodely task type identifier. |
| `teamId` | string | no | Filter tasks by team identifier. |
| `driverUserId` | string | no | Filter tasks by assigned driver user identifier. |
| `merchantId` | string | no | Filter tasks by merchant identifier. |
| `taskGuid` | string | no | Filter by the task GUID. |
| `externalKey` | string | no | Filter by the external task key. |
| `routeId` | string | no | Filter tasks by route identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of tasks to return. Example: `100`. |
| `lastId` | string | no | Cursor value from the previous response for pagination. Example: `6320AE1096`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "afterDateTime": "string",
      "alert": "string",
      "amountDue": 1,
      "assignedToDriverUserId": "string",
      "assignedToTeamId": 1,
      "beforeDateTime": "string",
      "capacity": 1,
      "completedCode": "string",
      "completedCoordinates": "string",
      "completedDateTime": "string",
      "completedNotes": "string",
      "completedRecipientName": "Ava Chen",
      "createdDateTime": "string",
      "deliveryFee": 1,
      "destinationAddress": "string",
      "destinationBuilding": "string",
      "destinationCoordinates": "string",
      "destinationNotes": "string",
      "dispatchAddress": "string",
      "dispatchBuilding": "string",
      "dispatchCoordinates": "string",
      "dispatchNotes": "string",
      "distance": 1,
      "driverName": "Ava Chen",
      "eta": "string",
      "externalKey": "string",
      "guid": "string",
      "id": 1,
      "lineCount": 1,
      "merchantId": "string",
      "merchantName": "Ava Chen",
      "modifiedDateTime": "string",
      "priority": 1,
      "recipientEmail": "ava@example.com",
      "recipientId": 1,
      "recipientName": "Ava Chen",
      "recipientPhone": "string",
      "requesterEmail": "ava@example.com",
      "requesterName": "Ava Chen",
      "requesterPhone": "string",
      "requirements": "string",
      "routeName": "Ava Chen",
      "routePlanId": 1,
      "routeSortId": 1,
      "serviceId": 1,
      "serviceName": "Ava Chen",
      "serviceTime": "string",
      "skills": "string",
      "statusColour": "string",
      "statusDesc": "string",
      "statusIcon": "string",
      "statusId": 1,
      "tag1": "string",
      "tag2": "string",
      "tag3": "string",
      "tag4": "string",
      "tag5": "string",
      "taskDesc": "string",
      "taskFailedReason": "string",
      "teamName": "Ava Chen",
      "templateData": "string",
      "templateId": 1,
      "templateName": "Ava Chen",
      "totalAmount": 1,
      "totalQty": 1,
      "totalWeight": 1,
      "typeDesc": "string",
      "typeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Account identifier. |
| `afterDateTime` | string | Complete-after timestamp in UTC. |
| `alert` | string | Notification alert setting. |
| `amountDue` | number | Amount due. |
| `assignedToDriverUserId` | string | Assigned driver user identifier. |
| `assignedToTeamId` | number | Assigned team identifier. |
| `beforeDateTime` | string | Complete-before timestamp in UTC. |
| `capacity` | number | Task capacity value. |
| `completedCode` | string | Completion code. |
| `completedCoordinates` | string | Completion coordinates. |
| `completedDateTime` | string | Completion timestamp in UTC. |
| `completedNotes` | string | Completion notes. |
| `completedRecipientName` | string | Completion recipient name. |
| `createdDateTime` | string | Task creation timestamp in UTC. |
| `deliveryFee` | number | Delivery fee. |
| `destinationAddress` | string | Destination address. |
| `destinationBuilding` | string | Destination building details. |
| `destinationCoordinates` | string | Destination coordinates. |
| `destinationNotes` | string | Destination notes. |
| `dispatchAddress` | string | Dispatch or pickup address. |
| `dispatchBuilding` | string | Dispatch or pickup building details. |
| `dispatchCoordinates` | string | Dispatch or pickup coordinates. |
| `dispatchNotes` | string | Dispatch or pickup notes. |
| `distance` | number | Distance value returned by Wodely. |
| `driverName` | string | Assigned driver name. |
| `eta` | string | Estimated arrival timestamp in UTC. |
| `externalKey` | string | External task key or barcode. |
| `guid` | string | Task GUID. |
| `id` | number | Numeric task identifier. |
| `lineCount` | number | Number of package lines. |
| `merchantId` | string | Merchant identifier. |
| `merchantName` | string | Merchant name. |
| `modifiedDateTime` | string | Task last modified timestamp in UTC. |
| `priority` | number | Priority identifier. |
| `recipientEmail` | string | Recipient email. |
| `recipientId` | number | Recipient identifier. |
| `recipientName` | string | Recipient name. |
| `recipientPhone` | string | Recipient phone. |
| `requesterEmail` | string | Requester or sender email. |
| `requesterName` | string | Requester or sender name. |
| `requesterPhone` | string | Requester or sender phone. |
| `requirements` | string | Proof-of-delivery requirements. |
| `routeName` | string | Route name. |
| `routePlanId` | number | Route plan identifier. |
| `routeSortId` | number | Route sort identifier. |
| `serviceId` | number | Service identifier. |
| `serviceName` | string | Service name. |
| `serviceTime` | string | Service time in minutes. |
| `skills` | string | Required or matched skills. |
| `statusColour` | string | Task status colour value. |
| `statusDesc` | string | Task status label. |
| `statusIcon` | string | Task status icon value. |
| `statusId` | number | Task status identifier. |
| `tag1` | string | Custom field 1. |
| `tag2` | string | Custom field 2. |
| `tag3` | string | Custom field 3. |
| `tag4` | string | Custom field 4. |
| `tag5` | string | Custom field 5. |
| `taskDesc` | string | Task description. |
| `taskFailedReason` | string | Task failure reason. |
| `teamName` | string | Assigned team name. |
| `templateData` | string | Template data payload. |
| `templateId` | number | Template identifier. |
| `templateName` | string | Template name. |
| `totalAmount` | number | Total task amount. |
| `totalQty` | number | Total package quantity. |
| `totalWeight` | number | Total task weight. |
| `typeDesc` | string | Task type label. |
| `typeId` | number | Task type identifier. |

## Native endpoint

Through the native Wodely API, this operation is `POST /v2/tasks/search` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tasks.md) for the provider-specific parameters and requirements.


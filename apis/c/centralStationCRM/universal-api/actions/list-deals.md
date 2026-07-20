# CentralStationCRM: List Deals

Retrieves all available deals from CentralStationCRM.

```
GET https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CentralStationCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/list-deals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/list-deals?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "companyId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "currentState": "string",
      "dealTypeId": 1,
      "dealTypeStageId": 1,
      "description": "string",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "groupId": 1,
      "id": 1,
      "name": "Ava Chen",
      "previousDealId": 1,
      "probability": 1,
      "targetDate": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedByUserId": 1,
      "userId": 1,
      "value": "string",
      "valueCount": "string",
      "valueSum": "string",
      "valueType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `companyId` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `currentState` | string |  |
| `dealTypeId` | number |  |
| `dealTypeStageId` | number |  |
| `description` | string |  |
| `finishedAt` | date |  |
| `groupId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `previousDealId` | number |  |
| `probability` | number |  |
| `targetDate` | date |  |
| `updatedAt` | date |  |
| `updatedByUserId` | number |  |
| `userId` | number |  |
| `value` | string |  |
| `valueCount` | string |  |
| `valueSum` | string |  |
| `valueType` | string |  |

## Native endpoint

Through the native CentralStationCRM API, this operation is `GET /api/deals` (base URL `https://api.centralstationcrm.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.


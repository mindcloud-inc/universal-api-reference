# CentralStationCRM: Create Project

Creates a new project in CentralStationCRM.

```
POST https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CentralStationCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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
      "background": "string",
      "companyId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentState": "string",
      "dealId": 1,
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "groupId": 1,
      "id": 1,
      "name": "Ava Chen",
      "targetDate": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `background` | string |  |
| `companyId` | number |  |
| `createdAt` | date |  |
| `currentState` | string |  |
| `dealId` | number |  |
| `finishedAt` | date |  |
| `groupId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `targetDate` | date |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native CentralStationCRM API, this operation is `POST /api/projects` (base URL `https://api.centralstationcrm.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.


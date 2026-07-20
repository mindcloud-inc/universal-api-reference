# CentralStationCRM: Create Company

Creates a new company in CentralStationCRM.

```
POST https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CentralStationCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-company', {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByUserId": 1,
      "groupId": 1,
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedByUserId": 1,
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
| `createdAt` | date |  |
| `createdByUserId` | number |  |
| `groupId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `updatedByUserId` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native CentralStationCRM API, this operation is `POST /api/companies` (base URL `https://api.centralstationcrm.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.


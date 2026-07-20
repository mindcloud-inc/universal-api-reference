# CentralStationCRM: Create Person

Creates a new person in CentralStationCRM.

```
POST https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CentralStationCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-person', {
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
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByUserId": 1,
      "firstName": "Ava",
      "gender": "string",
      "genderIdentity": "string",
      "groupId": 1,
      "id": 1,
      "name": "Ava Chen",
      "salutation": "string",
      "title": "string",
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
| `countryCode` | string |  |
| `createdAt` | date |  |
| `createdByUserId` | number |  |
| `firstName` | string |  |
| `gender` | string |  |
| `genderIdentity` | string |  |
| `groupId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `salutation` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `updatedByUserId` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native CentralStationCRM API, this operation is `POST /api/people` (base URL `https://api.centralstationcrm.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.


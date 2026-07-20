# CentralStationCRM: Get Person

Retrieves a single person from CentralStationCRM.

```
GET https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CentralStationCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/get-person?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/get-person?${params}`, {
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

Through the native CentralStationCRM API, this operation is `GET /api/people/:id` (base URL `https://api.centralstationcrm.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.


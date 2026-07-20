# CentralStationCRM: Search People

Finds people in CentralStationCRM by search term.

```
GET https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CentralStationCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/search-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/search-people?${params}`, {
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

Through the native CentralStationCRM API, this operation is `GET /api/people/search` (base URL `https://api.centralstationcrm.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.


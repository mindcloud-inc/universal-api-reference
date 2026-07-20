# TalentHR: List Time Off Blocked Periods

Retrieves blocked time off periods from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-time-off-blocked-periods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-time-off-blocked-periods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-time-off-blocked-periods?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isActive": true,
      "isForAll": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "timeOffTypes": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `endDate` | date |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isForAll` | number |  |
| `startDate` | date |  |
| `timeOffTypes` | array<object> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /blocked-time-offs` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-off-blocked-periods.md) for the provider-specific parameters and requirements.


# TalentHR: Create Time Off Blocked Period

Creates a new blocked time off period in TalentHR.

```
POST https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-time-off-blocked-period
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-time-off-blocked-period" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "startDate": "string",
  "endDate": "string",
  "isActive": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-time-off-blocked-period', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "startDate": "string",
    "endDate": "string",
    "isActive": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startDate` | string | yes | Blocked period start date in YYYY-MM-DD format. |
| `endDate` | string | yes | Blocked period end date in YYYY-MM-DD format. |
| `isActive` | boolean | yes | Whether the blocked period is active. |
| `timeOffType[]` | array<number> | no | Optional array of time off type IDs. Leave empty to apply to all types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "deletedAt": "string",
      "endDate": "string",
      "id": 1,
      "isActive": true,
      "isForAll": true,
      "startDate": "string",
      "timeOffTypes": [
        {}
      ],
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `deletedAt` | string |  |
| `endDate` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isForAll` | boolean |  |
| `startDate` | string |  |
| `timeOffTypes` | array<object> |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native TalentHR API, this operation is `POST /blocked-time-offs` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-off-blocked-period.md) for the provider-specific parameters and requirements.


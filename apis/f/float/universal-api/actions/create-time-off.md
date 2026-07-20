# Float: Create Time Off

Creates a new time off entry in Float.

```
POST https://connect.mindcloud.co/v1/universal/float/latest/actions/create-time-off
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/float/latest/actions/create-time-off" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timeoffTypeId": 1,
  "startDate": "string",
  "endDate": "string",
  "peopleIds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/float/latest/actions/create-time-off', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timeoffTypeId": 1,
    "startDate": "string",
    "endDate": "string",
    "peopleIds": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeoffTypeId` | number | yes | The ID of this time off type |
| `startDate` | string | yes | Start date of this time off |
| `endDate` | string | yes | End date of this time off |
| `hours` | number | no | Number of hours per day for this time off |
| `timeoffNotes` | string | no | Additional notes about the time off |
| `repeatState` | number | no | Frequency that this time off repeats |
| `status` | number | no | Status of the time off |
| `repeatEnd` | string | no | Date that the repeating time off will cease |
| `fullDay` | number | no | Whether this time off is for a full day |
| `peopleIds` | list<number> | yes | List of people IDs assigned to this time off |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "createdBy": 1,
      "endDate": "string",
      "fullDay": 1,
      "hours": {},
      "modified": "string",
      "modifiedBy": 1,
      "peopleIds": [
        1
      ],
      "repeatEnd": {},
      "repeatState": 1,
      "startDate": "string",
      "startTime": {},
      "status": 1,
      "statusCreatorId": {},
      "statusNote": {},
      "timeoffId": 1,
      "timeoffNotes": "string",
      "timeoffTypeId": 1,
      "timeoffTypeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `createdBy` | number |  |
| `endDate` | string |  |
| `fullDay` | number |  |
| `hours` | object |  |
| `modified` | string |  |
| `modifiedBy` | number |  |
| `peopleIds[]` | number |  |
| `repeatEnd` | object |  |
| `repeatState` | number |  |
| `startDate` | string |  |
| `startTime` | object |  |
| `status` | number |  |
| `statusCreatorId` | object |  |
| `statusNote` | object |  |
| `timeoffId` | number |  |
| `timeoffNotes` | string |  |
| `timeoffTypeId` | number |  |
| `timeoffTypeName` | string |  |

## Native endpoint

Through the native Float API, this operation is `POST /timeoffs` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-off.md) for the provider-specific parameters and requirements.


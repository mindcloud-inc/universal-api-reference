# TalentHR: Update Holiday

Updates an existing holiday in TalentHR.

```
PUT https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/update-holiday
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/update-holiday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectId": 1,
  "name": "Ava Chen",
  "holidayDate": "string",
  "requiredForAll": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/update-holiday', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectId": 1,
    "name": "Ava Chen",
    "holidayDate": "string",
    "requiredForAll": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectId` | number | yes | TalentHR holiday ID. |
| `name` | string | yes | Holiday name. |
| `holidayDate` | string | yes | Holiday date in YYYY-MM-DD format. |
| `requiredForAll` | boolean | yes | Whether the holiday applies to all employees. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "deletedAt": "string",
      "holidayDate": "string",
      "holidayRequiredFor": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "requiredForAll": true,
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
| `holidayDate` | string |  |
| `holidayRequiredFor` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `requiredForAll` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native TalentHR API, this operation is `PUT /holidays/:objectId` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-holiday.md) for the provider-specific parameters and requirements.


# TalentHR: Create Holiday

Creates a new holiday in TalentHR.

```
POST https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-holiday
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-holiday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "holidayDate": "string",
  "requiredForAll": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-holiday', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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

Through the native TalentHR API, this operation is `POST /holidays` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-holiday.md) for the provider-specific parameters and requirements.


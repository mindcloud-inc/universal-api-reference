# TalentHR: Create Time Off Type

Creates a new time off type in TalentHR.

```
POST https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-time-off-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-time-off-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "budget": 1,
  "paid": true,
  "isDisabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-time-off-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "budget": 1,
    "paid": true,
    "isDisabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Time off type name. |
| `budget` | number | yes | Time off budget. |
| `paid` | boolean | yes | Whether the time off type is paid. |
| `isDisabled` | boolean | yes | Whether the time off type is disabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowExceeding": true,
      "budget": "string",
      "calendarBlocking": true,
      "createdAt": "string",
      "deletedAt": "string",
      "id": 1,
      "isDefault": true,
      "isDisabled": true,
      "name": "Ava Chen",
      "needsApproval": true,
      "paid": true,
      "period": "string",
      "slug": "string",
      "updatedAt": "string",
      "visibleInternally": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowExceeding` | boolean |  |
| `budget` | string |  |
| `calendarBlocking` | boolean |  |
| `createdAt` | string |  |
| `deletedAt` | string |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `isDisabled` | boolean |  |
| `name` | string |  |
| `needsApproval` | boolean |  |
| `paid` | boolean |  |
| `period` | string |  |
| `slug` | string |  |
| `updatedAt` | string |  |
| `visibleInternally` | boolean |  |

## Native endpoint

Through the native TalentHR API, this operation is `POST /time-off-types` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-off-type.md) for the provider-specific parameters and requirements.


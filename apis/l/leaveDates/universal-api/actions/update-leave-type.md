# Leave Dates: Update Leave Type

Updates an existing leave type in Leave Dates.

```
PUT https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/update-leave-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/update-leave-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "companyId": "string",
  "allowanceTypeId": "string",
  "name": "Ava Chen",
  "displayCode": "string",
  "displayIcon": "string",
  "colour": "string",
  "approval": true,
  "isHoliday": true,
  "onlyAdmin": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/update-leave-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "companyId": "string",
    "allowanceTypeId": "string",
    "name": "Ava Chen",
    "displayCode": "string",
    "displayIcon": "string",
    "colour": "string",
    "approval": true,
    "isHoliday": true,
    "onlyAdmin": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `companyId` | string | yes |  |
| `allowanceTypeId` | string | yes |  |
| `name` | string | yes |  |
| `displayCode` | string | yes |  |
| `displayIcon` | string | yes |  |
| `colour` | string | yes |  |
| `approval` | boolean | yes |  |
| `isHoliday` | boolean | yes |  |
| `onlyAdmin` | boolean | yes |  |
| `description` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leave Dates API returns.

## Native endpoint

Through the native Leave Dates API, this operation is `PUT /leave-types/:id` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-leave-type.md) for the provider-specific parameters and requirements.


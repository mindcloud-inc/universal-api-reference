# Planday: Update Shift

Updates an existing shift in Planday.

```
PUT https://connect.mindcloud.co/v1/universal/planday/latest/actions/update-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planday/latest/actions/update-shift" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "allowConflicts": true,
  "date": "string",
  "employeeGroupId": 1,
  "shiftId": 1,
  "useBreaks": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planday/latest/actions/update-shift', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "allowConflicts": true,
    "date": "string",
    "employeeGroupId": 1,
    "shiftId": 1,
    "useBreaks": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowConflicts` | boolean | yes |  |
| `date` | string | yes |  |
| `employeeGroupId` | number | yes |  |
| `employeeId` | number | no |  |
| `endTime` | string | no |  |
| `positionId` | number | no |  |
| `shiftId` | number | yes |  |
| `shiftTypeId` | number | no |  |
| `startTime` | string | no |  |
| `useBreaks` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "departmentId": 1,
      "employeeGroupId": 1,
      "employeeId": 1,
      "endTime": "string",
      "id": 1,
      "positionId": 1,
      "startTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `departmentId` | number |  |
| `employeeGroupId` | number |  |
| `employeeId` | number |  |
| `endTime` | string |  |
| `id` | number |  |
| `positionId` | number |  |
| `startTime` | string |  |

## Native endpoint

Through the native Planday API, this operation is `PUT /scheduling/v1.0/shifts/:shiftId` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shift.md) for the provider-specific parameters and requirements.


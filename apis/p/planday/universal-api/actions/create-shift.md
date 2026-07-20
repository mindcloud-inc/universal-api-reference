# Planday: Create Shift

Creates a new shift in Planday.

```
POST https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-shift" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "allowConflicts": true,
  "date": "string",
  "departmentId": 1,
  "employeeGroupId": 1,
  "useBreaks": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-shift', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "allowConflicts": true,
    "date": "string",
    "departmentId": 1,
    "employeeGroupId": 1,
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
| `comment` | string | no |  |
| `date` | string | yes |  |
| `departmentId` | number | yes |  |
| `employeeGroupId` | number | yes |  |
| `employeeId` | number | no |  |
| `endTime` | string | no |  |
| `positionId` | number | no |  |
| `shiftTypeId` | number | no |  |
| `skillIds[]` | array<number> | no |  |
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
| `endTime` | string |  |
| `id` | number |  |
| `positionId` | number |  |
| `startTime` | string |  |

## Native endpoint

Through the native Planday API, this operation is `POST /scheduling/v1.0/shifts` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shift.md) for the provider-specific parameters and requirements.


# Planday: Create Position

Creates a new position in Planday.

```
POST https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "affectRevenue": true,
  "departmentId": 1,
  "employeeGroupId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-position', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "affectRevenue": true,
    "departmentId": 1,
    "employeeGroupId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `affectRevenue` | boolean | yes |  |
| `color` | string | no |  |
| `departmentId` | number | yes |  |
| `employeeGroupId` | number | yes |  |
| `name` | string | yes |  |
| `revenueUnitId` | number | no |  |
| `sectionId` | number | no |  |
| `skillIds[]` | array<number> | no |  |
| `validFrom` | date | no |  |
| `validTo` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affectRevenue": true,
      "departmentId": 1,
      "employeeGroupId": 1,
      "id": 1,
      "isActive": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affectRevenue` | boolean |  |
| `departmentId` | number |  |
| `employeeGroupId` | number |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Planday API, this operation is `POST /scheduling/v1.0/positions` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-position.md) for the provider-specific parameters and requirements.


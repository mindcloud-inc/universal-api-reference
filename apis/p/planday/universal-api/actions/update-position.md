# Planday: Update Position

Updates an existing position in Planday.

```
PUT https://connect.mindcloud.co/v1/universal/planday/latest/actions/update-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planday/latest/actions/update-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "affectRevenue": true,
  "name": "Ava Chen",
  "positionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planday/latest/actions/update-position', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "affectRevenue": true,
    "name": "Ava Chen",
    "positionId": 1
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
| `name` | string | yes |  |
| `positionId` | number | yes |  |
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

Through the native Planday API, this operation is `PUT /scheduling/v1.0/positions/:positionId` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-position.md) for the provider-specific parameters and requirements.


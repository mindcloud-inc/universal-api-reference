# Meisterplan: Update Role

Updates an existing role in Meisterplan.

```
PUT https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roleId` | string | yes |  |
| `name` | string | no |  |
| `externalId` | string | no |  |
| `costType` | string | no |  |
| `obsUnits` | object | no |  |
| `resourceManager` | object | no |  |
| `costPerHour` | number | no |  |
| `costPerHourValidFrom` | date | no |  |
| `costRates[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "costPerHour": 1,
      "costType": "string",
      "externalId": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `costPerHour` | number | Cost per hour |
| `costType` | string | Cost type |
| `externalId` | string | External ID |
| `id` | string | Role ID |
| `name` | string | Role name |

## Native endpoint

Through the native Meisterplan API, this operation is `PATCH /roles/:roleId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-role.md) for the provider-specific parameters and requirements.


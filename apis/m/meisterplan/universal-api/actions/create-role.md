# Meisterplan: Create Role

Creates a new role in Meisterplan.

```
POST https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
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

Through the native Meisterplan API, this operation is `POST /roles` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-role.md) for the provider-specific parameters and requirements.


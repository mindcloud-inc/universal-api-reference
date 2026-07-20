# Rentman: Create Project Function



```
POST https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-project-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-project-function" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "subproject": "string",
  "cost_rate": "string",
  "price_rate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-project-function', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "subproject": "string",
    "cost_rate": "string",
    "price_rate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Numeric ID of the parent project. |
| `subproject` | string | yes | Subproject reference, for example /subprojects/0. |
| `cost_rate` | string | yes | Cost rate reference, for example /rates/0. |
| `price_rate` | string | yes | Price rate reference, for example /rates/0. |
| `name` | string | no | Function name on packing lists. |
| `type` | string | no | Function type. |
| `amount` | number | no | Function amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "cost_rate": "string",
      "costs_variable": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "displayname": "Ava Chen",
      "duration": 1,
      "id": 1,
      "in_financial": true,
      "in_planning": true,
      "is_plannable": true,
      "ledger": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "price_rate": "string",
      "price_variable": 1,
      "project": "string",
      "subproject": "string",
      "taxclass": "string",
      "type": "string",
      "updateHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `cost_rate` | string |  |
| `costs_variable` | number |  |
| `created` | date |  |
| `creator` | string |  |
| `displayname` | string |  |
| `duration` | number |  |
| `id` | number |  |
| `in_financial` | boolean |  |
| `in_planning` | boolean |  |
| `is_plannable` | boolean |  |
| `ledger` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `price_rate` | string |  |
| `price_variable` | number |  |
| `project` | string |  |
| `subproject` | string |  |
| `taxclass` | string |  |
| `type` | string |  |
| `updateHash` | string |  |

## Native endpoint

Through the native Rentman API, this operation is `POST /projects/:id/projectfunctions` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-function.md) for the provider-specific parameters and requirements.


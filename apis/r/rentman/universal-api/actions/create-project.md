# Rentman: Create Project



```
POST https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Project name. |
| `reference` | string | no | Project reference. |
| `number` | string | no | Project number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_manager": "string",
      "color": "string",
      "conditions": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "cust_contact": "string",
      "custom": {},
      "customer": "string",
      "deposit_status": "string",
      "displayname": "Ava Chen",
      "id": 1,
      "loc_contact": "string",
      "location": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "number": 1,
      "project_type": "string",
      "reference": "string",
      "refundabledeposit": 1,
      "updateHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_manager` | string |  |
| `color` | string |  |
| `conditions` | string |  |
| `created` | date |  |
| `creator` | string |  |
| `cust_contact` | string |  |
| `custom` | object |  |
| `customer` | string |  |
| `deposit_status` | string |  |
| `displayname` | string |  |
| `id` | number |  |
| `loc_contact` | string |  |
| `location` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `number` | number |  |
| `project_type` | string |  |
| `reference` | string |  |
| `refundabledeposit` | number |  |
| `updateHash` | string |  |

## Native endpoint

Through the native Rentman API, this operation is `POST /projects` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.


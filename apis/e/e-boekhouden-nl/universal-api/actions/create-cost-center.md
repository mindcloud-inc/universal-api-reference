# e-Boekhouden.nl: Create Cost Center

Creates a new cost center in e-Boekhouden.nl.

```
POST https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-cost-center
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Boekhouden.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-cost-center" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-cost-center', {
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
| `description` | string | no | The description of the cost center. Error codes COST_003 Cost center description is required. COST_004 Cost center description is too long. COST_005 Cost center with this name already exists on this level of the tree. COST_011 Cost center fullPath is too long. COST_012 Cost center description has invalid characters. |
| `parentId` | number | no | The parent ID of the cost center. Error codes COST_005 Cost center with this name already exists on this level of the tree. COST_006 Cost center parent id cannot be changed. COST_007 Cost center parent is not active. COST_008 Cost center parent not found. |
| `active` | boolean | no | Whether the cost center is active. Error codes COST_007 Cost center parent is not active. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Boekhouden.nl API returns.

## Native endpoint

Through the native e-Boekhouden.nl API, this operation is `POST /v1/costcenter` (base URL `https://api.e-boekhouden.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cost-center.md) for the provider-specific parameters and requirements.


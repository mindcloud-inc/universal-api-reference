# ProfitWell: Update Plan

Updates a plan in ProfitWell.

```
PUT https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/update-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/update-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "foo_plan",
  "name": "New Plan Name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/update-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "foo_plan",
    "name": "New Plan Name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the manually-added plan you wish to retrieve or update. Example: `foo_plan`. |
| `name` | string | yes | The new name of the plan. Example: `New Plan Name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native ProfitWell API, this operation is `PUT /v2/plans/:id/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-plan.md) for the provider-specific parameters and requirements.


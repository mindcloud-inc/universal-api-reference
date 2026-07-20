# Tidely: Create Weekly Plan



```
POST https://connect.mindcloud.co/v1/universal/tidely/latest/actions/create-weekly-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tidely/latest/actions/create-weekly-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidely/latest/actions/create-weekly-plan', {
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
| `amount` | string | no | Plan amount. |
| `date` | string | no | Plan date in YYYY-MM-DD format. |
| `name` | string | no | Name of the Tidely plan. |
| `type` | string | no | Plan type. Use ONE_TIME. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the plan creation operation succeeded. |

## Native endpoint

Through the native Tidely API, this operation is `POST /api/v1/open-api/plans` (base URL `https://api.tidely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-weekly-plan.md) for the provider-specific parameters and requirements.


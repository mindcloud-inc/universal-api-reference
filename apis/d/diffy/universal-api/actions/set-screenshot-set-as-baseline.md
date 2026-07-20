# Diffy: Set Screenshot Set as Baseline

Sets a screenshot set as baseline in Diffy.

```
PUT https://connect.mindcloud.co/v1/universal/diffy/latest/actions/set-screenshot-set-as-baseline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/diffy/latest/actions/set-screenshot-set-as-baseline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "screenshotId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/diffy/latest/actions/set-screenshot-set-as-baseline', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "screenshotId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Project ID. |
| `screenshotId` | number | yes | Screenshot ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Diffy API returns.

## Native endpoint

Through the native Diffy API, this operation is `PUT /projects/:id/set-base-line-set/:screenshot_id` (base URL `https://app.diffy.website/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-screenshot-set-as-baseline.md) for the provider-specific parameters and requirements.


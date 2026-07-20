# FlexiFunnels: Mark Complete

Marks a lesson complete in FlexiFunnels.

```
PUT https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/mark-complete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlexiFunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/mark-complete" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "funnelPageId": "1027516",
  "courseId": "91090",
  "lessonId": "545366"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/mark-complete', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "funnelPageId": "1027516",
    "courseId": "91090",
    "lessonId": "545366"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `funnelPageId` | number | yes | Default: `1027516`. |
| `courseId` | number | yes | Default: `91090`. |
| `lessonId` | number | yes | Default: `545366`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FlexiFunnels API returns.

## Native endpoint

Through the native FlexiFunnels API, this operation is `POST /api/markecomplete` (base URL `https://bridge.flexifunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-complete.md) for the provider-specific parameters and requirements.

